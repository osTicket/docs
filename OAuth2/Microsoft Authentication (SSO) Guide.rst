.. |br| raw:: html

    <br>

Microsoft Authentication (SSO) Guide
====================================

Microsoft OAuth allows Agents and Users to sign into the helpdesk with their Microsoft account.

Configuration
-------------

Choose 'Microsoft' in the 'Add New Instance' menu

.. image:: ../_static/images/oauth-authentication/oauth44_microsoft_inst.png
  :alt: oauth44_microsoft_inst

|br|

Give the instance a name that lets you know which provider is selected and select 'Enabled' for the status.

.. image:: ../_static/images/oauth-authentication/oauth12_enable_inst.png
  :alt: oauth12_enable_inst

|br|

Go to the 'Config' tab to set up this provider. Some of the default information will be autofilled.

**Note:** The 'Authentication Label' field is the text that will be displayed to the User or Agent when they sign into the helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth13_inst_empty.png
  :alt: oauth13_inst_empty

|br|

Choose an Authentication Target to specify who should be able to use this provider.

.. image:: ../_static/images/oauth-authentication/oauth35_audience.png
  :alt: oauth35_audience

|br|

Now you need to set up an application using your Microsoft account. The first thing you need to do is log in to the `Azure Portal <https://portal.azure.com/#home>`_. which brings you to your Dashboard.

.. image:: ../_static/images/oauth-authentication/oauth1_azure_dashboard.png
  :alt: oauth1_azure_dashboard

|br|

**Note:** if you see an authentication issue, it means you are a standard user with restricted access.

.. image:: ../_static/images/oauth-authentication/oauth2_tenant_error.png
  :alt: oauth2_tenant_error

|br|

In order to use OAuth, you must have an account with administrative access to a tenant or you must be added to a tenant by an administrator.

Next, you'll need to go to 'Azure Active Directory' and click 'App Registrations'.

.. image:: ../_static/images/oauth-authentication/oauth85_app_regis.png
  :alt: oauth85_app_regis

|br|

Click 'New Registration'

.. image:: ../_static/images/oauth-authentication/oauth86_new_regis.png
  :alt: oauth86_new_regis

|br|

.. image:: ../_static/images/oauth-authentication/oauth87_registration_page.png
  :alt: oauth87_registration_page

|br|

Name the application and choose the supported account types:

**Note:** The supported account type will determine the 'Authorization Endpoint' and 'Token Endpoint' in your osTicket instance.

.. image:: ../_static/images/oauth-authentication/oauth41_act_type.png
  :alt: oauth41_act_type

|br|

The Redirect URI can be found in the plugin instance created in osTicket.

.. image:: ../_static/images/oauth-authentication/oauth15_blank_redir_uri.png
  :alt: oauth15_blank_redir_uri

|br|

.. image:: ../_static/images/oauth-authentication/oauth14_ost_redir_uri.png
  :alt: oauth14_ost_redir_uri

|br|

Choose Web for the Platform, paste in the Redirect URI, and click Register.

.. image:: ../_static/images/oauth-authentication/oauth16_filled_redir_uri.png
  :alt: oauth16_filled_redir_uri

|br|

Once you click Register, it will take you to the Overview for your new Application.

.. image:: ../_static/images/oauth-authentication/oauth19_overview.png
  :alt: oauth19_overview

|br|

Copy the 'Application (client) ID and paste it into the Client ID field in your osTicket plugin instance:

.. image:: ../_static/images/oauth-authentication/oauth20_azure_cid.png
  :alt: oauth20_azure_cid

|br|

.. image:: ../_static/images/oauth-authentication/oauth21_ost_cid.png
  :alt: oauth21_ost_cid

|br|

Go back to Azure and click 'Add a certificate or secret'

.. image:: ../_static/images/oauth-authentication/oauth22_add_secret.png
  :alt: oauth22_add_secret

|br|

Click 'New Client Secret' to generate a new Client Secret

.. image:: ../_static/images/oauth-authentication/oauth23_new_secret.png
  :alt: oauth23_new_secret

|br|

Add a secret description and click 'Add'

.. image:: ../_static/images/oauth-authentication/oauth24_secret_desc.png
  :alt: oauth24_secret_desc

**Important:** The secret 'Value' will only be shown once. If you lose this value, you will have to generate a new one.

.. image:: ../_static/images/oauth-authentication/oauth25_secret_val.png
  :alt: oauth25_secret_val

|br|

Copy the value and paste it into the 'Client Secret' field on the osTicket instance:

.. image:: ../_static/images/oauth-authentication/oauth26_ost_secret.png
  :alt: oauth26_ost_secret

|br|

Now you will need to get the Endpoint values from Azure. Go back to the 'Overview' tab and click the 'Endpoints' option.

.. image:: ../_static/images/oauth-authentication/oauth27_overview_endpoint.png
  :alt: oauth27_overview_endpoint

The supported account type chosen will determine the values for the 'Authorization Endpoint' and 'Token Endpoint' in your osTicket instance.

|br|

Single Tenant Endpoints:

.. image:: ../_static/images/oauth-authentication/oauth91_single.png
  :alt: oauth91_single

|br|

Multitenant Endpoints:

.. image:: ../_static/images/oauth-authentication/oauth89_multi1.png
  :alt: oauth89_multi1

|br|

Multitenant and Personal Accounts Endpoints:

.. image:: ../_static/images/oauth-authentication/oauth90_multi2.png
  :alt: oauth90_multi2

|br|

Personal Microsoft Account Endpoints:

.. image:: ../_static/images/oauth-authentication/oauth88_personal_only.png
  :alt: oauth88_personal_only

|br|

Copy the 'OAuth 2.0 authorization endpoint (v2)' and paste it into the 'Authorization Endpoint' field in the osTicket instance.

.. image:: ../_static/images/oauth-authentication/oauth92_azure_auth_end.png
  :alt: oauth92_azure_auth_end

|br|

.. image:: ../_static/images/oauth-authentication/oauth93_ost_auth_end.png
  :alt: oauth93_ost_auth_end

|br|

Copy the 'OAuth 2.0 token endpoint (v2)' and paste it into the 'Token Endpoint' field in the osTicket instance.

.. image:: ../_static/images/oauth-authentication/oauth94_azure_token_end.png
  :alt: oauth94_azure_token_end

|br|

.. image:: ../_static/images/oauth-authentication/oauth95_ost_token_end.png
  :alt: oauth95_ost_token_end

|br|

The rest of the information should be autofilled in the osTicket instance for you.

.. image:: ../_static/images/oauth-authentication/oauth96_ost_autofilled.png
  :alt: oauth96_ost_autofilled

|br|

Click 'Add Instance' and make sure you see a confirmation message.

.. image:: ../_static/images/oauth-authentication/oauth34_added_inst.png
  :alt: oauth34_added_inst

|br|

Now that the setup is complete, you should be able to use your Microsoft account to log into the helpdesk.

Agent Login
-----------

To test the functionality for Agents, go to:

Admin Panel | Agents

.. image:: ../_static/images/oauth-authentication/oauth36_backend.png
  :alt: oauth36_backend

|br|

Ensure that you see the provider that was just set up in the list. It is important, however, to make sure you choose **'Use any available backend'** so that you can still log into your helpdesk in the event that OAuth has an error.

**Note:** You must also ensure that the email for the Agent exists in the organization you are setting up OAuth for. You can see your users by going to Azure and clicking the 'Users' tab.

.. image:: ../_static/images/oauth-authentication/oauth40_azure_users.png
  :alt: oauth40_azure_users

|br|

Log out of the helpdesk and go to the login screen.

.. image:: ../_static/images/oauth-authentication/oauth37_login_screen.png
  :alt: oauth37_login_screen

|br|

Click the 'Sign in with Azure' button to test the OAuth set up.

**Note:** The sign in button text can be configured by changing the Authentication Label in the osTicket instance setup.

Now you will be prompted to enter your Microsoft account password.

.. image:: ../_static/images/oauth-authentication/oauth38_microsoft_pw.png
  :alt: oauth38_microsoft_pw

|br|

You may see a screen to allow osTicket to use your Microsoft login for the helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth39_permission.png
  :alt: oauth39_permission

|br|

Click Yes and you should be signed into your helpdesk as an Agent.

User Login
----------

For users, logging in with a Microsoft account should create a new User if one does not exist, otherwise, it will log in as an existing User.

.. image:: ../_static/images/oauth-authentication/oauth80_user_portal.png
  :alt: oauth80_user_portal

|br|

Click 'Sign In'

.. image:: ../_static/images/oauth-authentication/oauth83_user_login.png
  :alt: oauth83_user_login

|br|

Click 'Sign in with Azure'. Now you will be prompted to enter your Microsoft account password.

.. image:: ../_static/images/oauth-authentication/oauth84_choose_outlook.png
  :alt: oauth84_choose_outlook

|br|

Choose your account and you should be logged in as a User.

.. image:: ../_static/images/oauth-authentication/oauth97_user_logged_in.png
  :alt: oauth97_user_logged_in
