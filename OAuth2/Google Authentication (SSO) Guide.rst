.. |br| raw:: html

    <br>

Google Authentication (SSO) Guide
=================================

Google OAuth allows Agents and Users to sign into the helpdesk with their Google account.

Configuration
-------------

Choose 'Google' in the 'Add New Instance' menu

.. image:: ../_static/images/oauth-authentication/oauth43_google_inst.png
  :alt: oauth43_google_inst

|br|

Give the instance a name that lets you know which provider is selected and select 'Enabled' for the status.

.. image:: ../_static/images/oauth-authentication/oauth42_enable_inst.png
  :alt: oauth42_enable_inst

|br|

Go to the 'Config' tab to set up this provider. Some of the default information will be autofilled.

**Note:** The 'Authentication Label' field is the text that will be displayed to the User or Agent when they sign into the helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth45_google_cfg.png
  :alt: oauth45_google_cfg

|br|

Choose an Authentication Target to specify who should be able to use this provider.

.. image:: ../_static/images/oauth-authentication/oauth46_audience.png
  :alt: oauth46_audience

|br|

Now you need to set up a project using the `Google Developer Console <https://console.developers.google.com/>`_.

Once you are in the console, click 'Select a Project' to get started.

**Note:** If you already have a project set up for your Google account, its name will be displayed here.

.. image:: ../_static/images/oauth-authentication/oauth47_google_proj.png
  :alt: oauth47_google_proj

|br|

Click 'New Project' in the modal:

.. image:: ../_static/images/oauth-authentication/oauth49_google_proj.png
  :alt: oauth49_google_proj

|br|

Give the project a name and click 'Create'

.. image:: ../_static/images/oauth-authentication/oauth50_create_proj.png
  :alt: oauth50_create_proj

|br|

Click 'OAuth consent screen'

.. image:: ../_static/images/oauth-authentication/oauth51_consent.png
  :alt: oauth51_consent

|br|

Choose your target users and click 'Create'

.. image:: ../_static/images/oauth-authentication/oauth52_audience.png
  :alt: oauth52_audience

|br|

Name your app and fill in your support email. Optionally, you can upload a logo.

.. image:: ../_static/images/oauth-authentication/oauth53_appinfo.png
  :alt: oauth53_appinfo

|br|

You can add your website URL if you will be using a domain that you own.

.. image:: ../_static/images/oauth-authentication/oauth54_app_domain.png
  :alt: oauth54_app_domain

|br|

Add your contact information:

.. image:: ../_static/images/oauth-authentication/oauth55_contact.png
  :alt: oauth55_contact

|br|

Scopes can be set to extend the permissions between your application and Gmail accounts. You do not need to add any scopes to use OAuth for a typical Gmail account.

.. image:: ../_static/images/oauth-authentication/oauth56_scopes1.png
  :alt: oauth56_scopes1

|br|

.. image:: ../_static/images/oauth-authentication/oauth57_scopes2.png
  :alt: oauth57_scopes2

|br|

Add addresses for emails you want to test with this application. Applications that are in 'Testing' mode can add up to 100 test users.

**Note:** The addresses must be valid Gmail accounts.

.. image:: ../_static/images/oauth-authentication/oauth99_test_users.png
  :alt: oauth99_test_users

|br|

.. image:: ../_static/images/oauth-authentication/oauth911_save_users.png
  :alt: oauth911_save_users

|br|

Click 'Save and Continue' to see an App Summary.

.. image:: ../_static/images/oauth-authentication/oauth61_summary1.png
  :alt: oauth61_summary1

|br|

Once saved, navigate to the 'Credentials' section

.. image:: ../_static/images/oauth-authentication/oauth63_creds.png
  :alt: oauth63_creds

|br|

Click 'Create Credentials' and select 'OAuth client ID'

.. image:: ../_static/images/oauth-authentication/oauth64_creds.png
  :alt: oauth64_creds

|br|

Choose 'Web Application' and name the App

.. image:: ../_static/images/oauth-authentication/oauth66_create_creds.png
  :alt: oauth66_create_creds

|br|

The Authorized redirect URI can be found in the plugin instance created in osTicket.

.. image:: ../_static/images/oauth-authentication/oauth67_blank_redir_uri.png
  :alt: oauth67_blank_redir_uri

|br|

.. image:: ../_static/images/oauth-authentication/oauth68_ost_redir_uri.png
  :alt: oauth68_ost_redir_uri

|br|

Click 'Add URI' from the Google console

.. image:: ../_static/images/oauth-authentication/oauth69_google_redir_uri.png
  :alt: oauth69_google_redir_uri

|br|

The Authorized JavaScript is just your hostname without anything extra at the end.

.. image:: ../_static/images/oauth-authentication/oauth70_js_origin.png
  :alt: oauth70_js_origin

|br|

Add the JavaScript origin and click 'Create'.

.. image:: ../_static/images/oauth-authentication/oauth71_js_origin.png
  :alt: oauth71_js_origin

|br|

Now you will see your Client ID and Client Secret

.. image:: ../_static/images/oauth-authentication/oauth72_client_info.png
  :alt: oauth72_client_info

|br|

Copy the Client ID and Client Secret and paste them into the appropriate fields in the osTicket Instance:

.. image:: ../_static/images/oauth-authentication/oauth73_ost_client_info.png
  :alt: oauth73_ost_client_info

|br|

The rest of the information should be autofilled

.. image:: ../_static/images/oauth-authentication/oauth74_autofilled.png
  :alt: oauth74_autofilled

|br|

Click 'Add Instance'

.. image:: ../_static/images/oauth-authentication/oauth75_google_add_inst.png
  :alt: oauth75_google_add_inst

|br|

Now that the setup is complete, you should be able to use your Google account to log into the helpdesk.

Agent Login
-----------

To test the functionality for Agents, go to:

Admin Panel | Agents

.. image:: ../_static/images/oauth-authentication/oauth76_gmail_agent.png
  :alt: oauth76_gmail_agent

|br|

Make sure you have an Agent in your helpdesk with the same email address as the Google account you want to log in with.

You should also ensure that you see the provider that was just set up in the list. It is important, however, to make sure you choose **'Use any available backend'** so that you can still log into your helpdesk in the event that OAuth has an error.

Log out of the helpdesk and go to the login screen.

.. image:: ../_static/images/oauth-authentication/oauth77_login_screen.png
  :alt: oauth77_login_screen

|br|

Click the 'Sign in with Google' button to test the OAuth set up.

**Note:** The sign in button text can be configured by changing the Authentication Label in the osTicket instance setup.

.. image:: ../_static/images/oauth-authentication/oauth77_login_screen.png
  :alt: oauth77_login_screen

|br|

This should navigate to choose the Google account you want to sign in with

.. image:: ../_static/images/oauth-authentication/oauth78_choose_gmail.png
  :alt: oauth78_choose_gmail

|br|

Now you should be logged into your helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth79_google_logged_in.png
  :alt: oauth79_google_logged_in

|br|

User Login
----------

For users, logging in with a Gmail account should create a new User if one does not exist, otherwise, it will log in as an existing User.

.. image:: ../_static/images/oauth-authentication/oauth80_user_portal.png
  :alt: oauth80_user_portal

|br|

.. image:: ../_static/images/oauth-authentication/oauth81_user_login.png
  :alt: oauth81_user_login

|br|

This should also navigate to choose the Google account you want to sign in with.

.. image:: ../_static/images/oauth-authentication/oauth78_choose_gmail.png
  :alt: oauth78_choose_gmail

|br|

Choose your account and you should be logged in as a User.

.. image:: ../_static/images/oauth-authentication/oauth97_user_logged_in.png
  :alt: oauth97_user_logged_in

|br|
