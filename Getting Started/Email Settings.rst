Email Settings
==============

osTicket allows you to setup unlimited number of email addresses to handle all your company's mail accounts and email communication. Incoming emails are converted to support tickets allowing you to easily manage, organize and archive all emailed support requests in one place.

Email Templates
---------------

osTicket ships with generic email templates used for auto-responses, alerts, notices and replies. Refer to :doc:`Email Templates Guide <Email Templates>` for details on how to customize or add new templates.

Routing Incoming Emails
-----------------------

Setting up your system to accept emails varies from system to system and depends on your personal preference. osTicket currently supports piping (aliases) and POP3/IMAP polling methods for routing incoming emails. Tickets are routed to the department and assigned a default priority associated with the email.

To enable incoming email fetching, in the Admin panel go to Settings and Email, and check the box for Email Fetching to enable it. It is disabled by default.

**EMAIL PIPING**

Piping method allows for real-time email handling. Extra setup is required at mail server level to pipe the raw email message to osTicket pipe handler. Both remote and local piping are supported. See :doc:`Email Piping Guide <Email Piping>`.

**POP3/IMAP POLLING**

POP3/IMAP account polling method is best suited for individuals with remote mail account(s) and/or with limited access to mail delivery settings. Each email address added to the system can have an account associated to it. See :doc:`POP3/IMAP Setting Guide <POP3-IMAP Settings>`.

Outgoing Emails
---------------

By default osTicket uses native PHP Mail function to send outgoing emails. However, this can be problematic to spam filters depending on your php.ini mail settings. It is highly recommended that you use SMTP instead.

Each of the email accounts can have it's own SMTP. You can also setup a default SMTP system wide. See Settings tab in admin panel.

**IMPORTANT NOTE REGARDING USE OF EXTERNAL SMTP SERVERS**

Some hosting companies (Hostgator.com, for example) do not allow the use of SMTP servers located on a separate server and will block all requests. Trying to connect to a blocked external SMTP server will result in a "login failure" message in OSTicket when trying to save the Outgoing Emails settings.

If you have shell access with your hosting account you can manually test a connection to a remote SMTP server from the command line using telnet:

.. code-block:: bash

  telnet smtp.example.com 25

A blocked connection will result in a message similar to the following:

.. code-block:: bash

  Trying 192.0.32.10...
  telnet: connect to address 192.0.32.10: Connection refused

**OUTGOING SMTP SPOOFING**

Check "Allow spoofing (No Overwrite)" in :code:`Settings => Email Settings`

Gmail Configuration
-------------------

In order to use Gmail, your host must support SSL, so osTicket can negotiate the secure connection, and you must enable IMAP or POP in your GMail or GApps account. Configure in osTicket (the easy part)

Under Admin panel -> Emails -> Emails -> Sending email via SMTP For most people, enter either ssl://smtp.gmail.com with port 465 or tls://smtp.gmail.com with port 587.

*note: If you have a google apps/G-Suite account, this might change, see below.*

Select "Authentication Required". Leave Header Spoofing unchecked. Make sure your username is your full email and password are set correctly in the Email Login Information

If you test at this point and it doesn't work, continue reading.

You may need to consult your PHP error log (the location varies by OS and personal preferences so consult your php.ini to determine its location). The PHP error log often contains more information as to why something is not working correctly.

**Check your Firewall**

Connection Refused errors are most likely caused by your firewall.

If you are running csf, it defaults to block outgoing SMTP connections. You can either turn off SMTP_BLOCK (not recommended) or add the user osTicket is running under to SMTP_ALLOWUSER. Also make sure the port you are using (465 or 587) is in SMTP_PORTS.

If you are running some other firewall, make sure it is allowing outgoing connections on 465 or 587.

*note: if you are running SELinux please disable it to see if that makes this start working. If it does then SELinux is blocking the connection and you will need to re-enable it and write a rule to allow the connection.*

**Check Gmail**

Not related to SMTP, but make sure you enabled IMAP or POP3 from Settings -> Forwarding and POP/IMAP

To enable `POP for your Gmail account <https://support.google.com/mail/answer/7104828?hl=en>`_.

To enable `IMAP for your Gmail account <https://support.google.com/mail/answer/7126229?hl=en>`_.

You may need to "allow less secure apps". From gmail, click your avatar at the top right of the page and click "My Account". In the left menu, under Sign-In & Security, click "Connected Apps and Sites". Scroll down to "Allow less secure apps" and turn it on and retest.

It is recommended to not leave this on unless necessary.

**Check your G-Suite policies**

G-Suite allows you to use their SMTP Relay service. This service allows you to open up SMTP under certain conditions. To use this service, you must configure it under Apps -> G-Suite > Gmail > Advanced Settings -> General Settings -> Routing Add an SMTP relay service with the appropriate settings. Make sure you change your osTicket configuration to use smtp-relay.gmail.com as the SMTP server.

See https://support.google.com/a/answer/2956491?hl=en for more information.
