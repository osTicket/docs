Licensed/Personal Emails
========================

If you are using a real, licensed email or a personal email follow the below steps to ensure you are up-to-date with the latest Microsoft deprecations:

#. Open a private browsing window. This is an important step to ensure you authorize the proper account and not your personal account, etc.
#. Login to your osTicket helpdesk.
#. Go to your system Emails (**Admin Panel > Emails > Emails**).
#. Click on a system email with OAuth2 configured.
#. Go to the **Remote Mailbox** tab.
#. Click the **Config** button.
#. Click the **Idp Config** tab.
#. Completely replace the **Scopes** value with the following:
   :code:`offline_access https://outlook.office.com/IMAP.AccessAsUser.All https://outlook.office.com/POP.AccessAsUser.All https://outlook.office.com/SMTP.Send`
#. Click **Submit**.
#. A pop up will be presented for you to sign in. It's important that you sign in to the email account you are configuring in osTicket; otherwise you will authorize the wrong account.
#. Now you should have a new token and should be able to **Save Changes** successfully.
#. Check the **Outgoing (SMTP)** tab to see if separate OAuth2 credentials are configured (ie. if **Authentication** is set to "OAuth2 - Microsoft"). If so, repeat these steps for the SMTP tab as well.
#. Repeat the above steps for each email you have configured in osTicket.
