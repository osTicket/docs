.. _pop3-imap-settings::

POP3/IMAP Settings Guide
========================

If email piping is not a preferred option for you or if your hosting provider does not support it, you may use POP3/IMAP account polling instead. osTicket will poll an external POP3/IMAP account on a regular basis, retrieve email messages and convert them to tickets. It is best suited for individuals with remote mail account(s) and/or limited access to mail delivery settings.

#. Enable mail fetch in :code:`Admin Panel => Settings => Email Settings`
#. Refer to your hosting manual or contact your hosting provider for host name and port number
#. Configure fetch frequency for each of the accounts - 5 minutes recommended
#. Enable *Delete fetched message(s)* - if your mail server doesn't support auto-archiving on fetch

Schedule Polling
----------------

**IMPORTANT:** Simply checking :code:`Admin Panel => Settings => Email Settings => Enable POP/IMAP email fetch` will not cause osTicket to automatically poll a mailbox for new messages. Account polling, unlike email piping, requires that a mail fetcher (script) be scheduled for repeated execution. Choose one of the methods below depending on your hosting environment.

**RECURRING TASKS SCHEDULER (CRON JOB)**

This is the most convenient method if your hosting provider allows scheduling recurring tasks via crontab on nix or "Scheduled Tasks" on a Windows server. Please refer to your hosting manual or contact your hosting provider for instructions. The PHP CLI executable is called to run cron.php.

Add the following entry to cron file normally in /etc/crontab in nix systems and adjust: the time; the webuser; and paths accordingly.

.. code-block:: bash

  */5 * * * * nobody /path/to/php /path/to/api/cron.php


For windows users in "Scheduled Tasks" add :code:`"c:\php\bin\php.exe c:\website\osticket\api\cron.php"`

**RECURRING TASKS SCHEDULER (HOST'S CUSTOM TASK SCHEDULER)**

Some hosts do not allow adding cron jobs, and instead only allow you to probe scripts located at a publicly accessible URL. In this case, you will schedule the task using your webhost's scheduling interface and http://domain/path/to/osticket/api/cron.php.

To prevent unauthorized execution of scripts from the outside, :code:`Settings => API` has rules for allowing external access based on originating IP and an API "passphrase", which is actually the User Agent string of the agent trying to access cron.php on your web server.

If the User Agent string is not changed to the API key, the request will be denied, email will not be polled, and :code:`API error - code #77: Unknown remote host 181.222.32.12 or invalid API key [Mozilla/5.0 (X11; U; Linux x86_64; en-US) AppleWebKit/534.13 (KHTML, like Gecko) Chrome/9.0.597.84 Safari/534.13]` will appear in your system logs under the osTicket dashboard.

If your host allows you to modify their schedulers User Agent string, then change that to the API key and add your webhost scheduler's IP to :code:`Settings => API => API Keys`.

**EXTERNAL TRIGGERING USING WGET**

First add an API key and IP to :code:`Settings => API => API Keys`.

#. Enter the IP of the host that the wget will run from.
#. Enter 3 separate words into the passphrase box (these are used in conjunction with the IP to generate hashes)
#. Click submit
#. A hash will be generated

Then, setup a cron job to run wget :code:`*/5 * * * * nobody wget -q -O /dev/null --user-agent=<API key here> http://<host & path goes here>/api/cron.php`

See `forum post <https://forum.osticket.com/d/9214-calling-remote-mail-fetch-from-another-server-using-cron/2>`_.

**AUTO CRON**

This is internal task manager triggered by staff's activity, no external setup required! If enabled, emails are fetched based on activity of a logged in staff member at an interval set for each of the email accounts.

#. Enable in :code:`Admin Panel => Emails => Settings` and ensure Email Fetching `Fetch on auto-cron` is enabled.
#. Please note that nothing happens if no one is logged in.
#. It might slow the page load a little in some instances.
#. Maximum of one cron call every 3 minutes per staff
