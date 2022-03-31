Email Piping
============

The email piping is a technique of sending email message as an input to a program rather than appending the message to the mailbox file, allowing for real-time email delivery and handling. Every mail server has its own rules and procedures for mail delivery, making it hard to provide common instructions for configuring an MTA. You should refer to your hosting manual or contact your hosting provider for email piping instructions if none of the methods below works for you.

#. osTicket supports both remote and local piping
#. Email piping must be enabled in admin panel Note: This option appears to be removed from v1.7 - piping works without enabling.

Local Piping
------------

Local piping refers to the case where osTicket is installed on a server also handling your emails. Most shared hosting users fall into this category.

**SETTING UP ALIASES IN CPANEL**

Add a forwarding rule for each of the email addresses to :code:`/path/to/api/pipe.php`.

For example forward support@domain.com to :code:`"|/path/to/api/pipe.php"`

CPANEL X INSTRUCTIONS

CPANEL -> Email -> Forwarders -> Add Forwarder

1. Address to a forwarder: @domain
2. Advanced Options -> Pipe to a Program:  :code:`public_html/osticket/api/pipe.php`
3. Click 'Add Forwarder' button

When complete you will see:

:code:`@domain to |/home//public_html/osticket/api/pipe.php`

#. assumption is you unpackaged osticket.tar in /home/USERNAME/public_html/
#. Pipe to a Program path: if you have a leading '/' cPanel will use the path you enter, if you do not have '/' cPanel will create it relative to your home directory
#. pipe.php should have hashbang at the top of the file: #!/usr/bin/php -q
#. Make pipe.php executable chmod 755 pipe.php
#. Enable email piping in admin panel Settings -> preference  Note: This option appears to be removed from v1.7 - piping works without enabling.

MAIL DELIVERY FAILED

If you have the error: 'Mail delivery failed: returning message to sender' but the user's email is still successfully processed.

You have some options:

**1. Update php.ini**

/usr/local/lib/php.ini update: display_errors Off

restart apache

**2. Update exim.conf**

Update /etc/exim.conf in the section:

address_pipe:

.. code-block:: bash

  driver = pipe
  return_output

virtual_address_pipe:

.. code-block:: bash

  driver = pipe
  group = "${lookup{$domain}lsearch* {/etc/userdomains}{$value}}"
  return_output
  user = "${lookup{$domain}lsearch* {/etc/userdomains}{$value}}"

Change **return_output** to **return_fail_output**

REASON: (from exim.conf comment)

If the pipe generates any standard output, it is returned to the sender of the message as a delivery error. Set return_fail_output instead of return_output if you want this to happen only when the pipe fails to complete normally. You can set different transports for aliases and forwards if you want to - see the references to address_pipe below.

**SETTING UP ALIASES WITH QMAIL**

Create/Edit your :code:`.qmail-*` for the domain you wish to forward and add a forwarding rule to :code:`/path/to/api/pipe.php`. For example for support@domain.com .qmail-support file should contain :code:`|/path/to/api/pipe.php`

**SETTING UP ALIASES FOR SENDMAIL**

Modify your aliases file by adding :code:`support: root, |/path/to/api/pipe.php` and run newaliases.

**SETTING UP ALIASES IN .PROCMAILRC**

.. code-block:: bash

  :0 c
     * ^To.*support@domain.com
     |/path/to/api/pipe.php


**SETTING UP ALIASES IN PLESK (POSTFIX)**

See this `blog post from Dave <http://blog.absolutedisaster.co.uk/osticket-plesk-9-postfix-pipe-mail-to-a-progr/>`_.

**Remote Piping**

Remote piping is useful when osTicket installation and the mail server are on two separate machines. To maintain logic in one place remote piping is done over HTTP post to osTicket's API. osTicket ships with two scripts to help you accomplish this task; :code:`automail.php` and :code:`automail.pl`. Both accomplish the same task by posting to http://www.yourdomain.com/osticket/api/tickets.email (replace osticket with the folder name where you installed osticket)

#. Remote host IP must be white listed in Admin Panel > Manage > API Keys
#. Valid API key required
#. Follow local piping instructions above to pipe emails to remote script which will in turn post to osTicket

For technical details, please refer to :doc:`API Docs <../Developer Documentation/API Docs>`.
