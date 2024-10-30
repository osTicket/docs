Shared Mailboxes/Resource Emails/Aliases
========================================

If you are using a shared mailbox, resource email, and/or alias email follow the below steps to ensure you are up-to-date with the latest Microsoft deprecations:

#. Open a private browsing window. This is an important step to ensure you authorize the proper account and not your personal account, etc.
#. Login to your osTicket helpdesk.
#. Go to your system Emails (**Admin Panel > Emails > Emails**).
#. Click on a system email with OAuth2 configured.
#. Go to the **Remote Mailbox** tab.
#. Click the **Config** button.
#. Within the **Info** tab, disable (*uncheck*) the setting for **Strict Matching**.
#. Click the **Idp Config** tab.
#. Completely replace the **Scopes** value with the following:
   :code:`offline_access https://outlook.office.com/IMAP.AccessAsUser.All https://outlook.office.com/POP.AccessAsUser.All https://outlook.office.com/SMTP.Send`
#. Click **Submit**.
#. A pop up will be presented for you to sign in. It's important that you sign in to the Service Account/User Account that has **Send As** and **Read and Manage** permissions to the shared mailbox/resource email/alias.
#. Now you should have a new token and should be able to **Save Changes** successfully.
#. If you get an error about mismatching emails on the first submission, simply resubmit the popup and it should go through the second time.
#. Check the **Outgoing (SMTP)** tab to see if separate OAuth2 credentials are configured (ie. if **Authentication** is set to "OAuth2 - Microsoft"). If so, repeat these steps for the SMTP tab as well.
#. Repeat the above steps for each email you have configured in osTicket.
