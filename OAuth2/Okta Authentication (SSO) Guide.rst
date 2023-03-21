.. |br| raw:: html

    <br>

Okta Authentication (SSO) Guide
===============================

Okta OAuth2 allows Agents and Users to sign into the helpdesk with their Okta account.

Configuration
-------------

Choose 'Okta' in the 'Add New Instance' menu

.. image:: ../_static/images/oauth-authentication/oauth2_okta_inst.png
  :alt: Add New Instance menu￼

|br|

Give the instance a name that lets you know which provider is selected and select 'Enabled' for the status.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_enable_inst.png
  :alt: Enable New Instance

|br|

Go to the 'Config' tab to set up this provider. Some of the default information will be autofilled.

**Note:** The 'Authentication Label' field is the text that will be displayed to the User or Agent when they sign into the helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_cfg.png
  :alt: OAuth2 Instance Config

|br|

Choose an Authentication Target to specify who should be able to use this provider.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_target_audience.png
  :alt: Authentication Target Audience

|br|

Now you need to set up a project using the Okta Admin Console. To visit the Admin Console simply login to Okta and click the button labeled Admin on the top bar next to your username.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_admin_console.png
  :alt: Okta Admin Console

Once you are in the console expand the Applications section, click Applications, and click 'Create App Integration' to get started.

**Note:** If you already have a project set up for your Okta account, its name will be displayed here.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_create_app.png
  :alt: Create App Integration

|br|

Click 'OIDC - OpenID Conect', 'Web Application', and 'Next' in the modal:

.. image:: ../_static/images/oauth-authentication/oauth2_okta_app_info.png
  :alt: Okta App Integration Setup Info

|br|

Give the project a name in the 'App Integration name'.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_app_integration_name.png
  :alt: App Integration Name

|br|

The 'Sign-in redirect URI' can be found in the plugin instance created in the helpdesk under the field labeled 'Redirect URI'.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_redirect_uri.png
  :alt: Redirect URI

|br|

.. image:: ../_static/images/oauth-authentication/oauth2_okta_signin_redirect_uri.png
  :alt: Sign-in redirect URI

|br|

Completely remove the default value in the 'Sign-out redirect URIs' field (ie. make it blank).

.. image:: ../_static/images/oauth-authentication/oauth2_okta_signout_before.png
  :alt: Sign-out redirect URIs Before

|br|

.. image:: ../_static/images/oauth-authentication/oauth2_okta_signout_after.png
  :alt: Sign-out redirect URIs After

|br|

Configure 'Assignments' by selecting one of the options or configure it later by selecting 'Skip group assignment for now' and click 'Save'.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_config_assignments.png
  :alt: Configure Assignments

|br|

Now you will see your Client ID and Client Secret

.. image:: ../_static/images/oauth-authentication/oauth2_okta_client_info.png
  :alt: Copy Client ID and Client Secret

|br|

Copy the Client ID and Client Secret and paste them into the appropriate fields in the helpdesk Instance:

.. image:: ../_static/images/oauth-authentication/oauth2_okta_client_info_after.png
  :alt: Paste Client ID and Client Secret

|br|

The remaining details are autofilled defaults that will need updating:

.. image:: ../_static/images/oauth-authentication/oauth2_okta_defaults.png
  :alt: Autofilled Defaults

|br|

For 'Authorization Endpoint', 'Token Endpoint', and 'Resource Details Endpoint' you must replace the :code:`${yourOktaDomain}` with your actual Okta Domain. This can be found by logging into the Okta Admin Console, click your name/email in the top right, and copy the domain under your email address.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_domain.png
  :alt: Okta Domain

|br|

Once you add your Okta Domain to the three Endpoints, they should look something like the following:

.. image:: ../_static/images/oauth-authentication/oauth2_okta_endpoints_after.png
  :alt: Endpoints After Update

|br|

The last section to configure in the instance config is the User Attributes Mapping section. To review your current Okta Attributes go to the Okta Admin Console, expand the Directory section on the left side, click Profile Editor, click the Application for the helpdesk, and scroll down to the Attributes section.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_profile_editor.png
  :alt: Profile Editor

|br|

.. image:: ../_static/images/oauth-authentication/oauth2_okta_attributes.png
  :alt: Okta Attributes

|br|

Here you will copy the 'Variable Name' value for each of the attributes needed for the helpdesk. So you will copy the Variable Name for Username (:code:`userName`), Given Name (:code:`given_name`), Family Name (:code:`family_name`), and Email (:code:`email`). **Please note**, the Variable Name values in your instance might be different than the ones shown in the screenshot above, depending on your setup and company policies.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_attr_mappings.png
  :alt: User Attribute Mappings

|br|

Once you've replaced the Attributes in the Plugin Instance config you are ready to add the instance. Click 'Add Instance'

.. image:: ../_static/images/oauth-authentication/oauth2_okta_add_instance.png
  :alt: Add Instance

|br|

If you chose the 'Skip group assignment for now' option in the earlier steps the very last thing to configure within Okta is to Assign Users to the Application. Go to the Application in the Okta Admin Console and click Assignments.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_config_assignments_2.png
  :alt: Configure Assignments

|br|

Here you will click 'Assign' then 'Assign To People' or 'Assign To Groups'. Assign the relevant Users/Groups and click 'Done'. Once Users/Groups are assigned they will be able to use Okta Authentication for the helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_choose_assignment.png
  :alt: Assign to People or Groups

|br|

Now that the setup is complete, you should be able to use your Okta account to log into the helpdesk.

Agent Login
-----------

To test the functionality for Agents, go to:

Admin Panel | Agents

.. image:: ../_static/images/oauth-authentication/oauth2_okta_add_agent.png
  :alt: Add New Agent

|br|

Make sure you have an Agent in your helpdesk with the same username or email address as the Okta account you want to log in with.

You should also ensure that you see the provider that was just set up in the list. It is important, however, to make sure you choose **'Use any available backend'** so that you can still log into your helpdesk in the event that OAuth has an error.

Log out of the helpdesk and go to the login screen.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_agent_login.png
  :alt: Agent Login Page

|br|

Click the 'Sign in with Okta' button to test the OAuth set up.

**Note:** The sign in button text can be configured by changing the Authentication Label in the instance setup.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_auth_label.png
  :alt: Authentication Label

|br|

This should navigate to Okta and have you login to the account you want to sign into the helpdesk with:

.. image:: ../_static/images/oauth-authentication/oauth2_okta_signin.png
  :alt: Okta Sign-in Page

|br|

Now you should be logged into your helpdesk.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_agent_logged_in.png
  :alt: Agent Logged In

|br|

User Login
----------

For users, logging in with a Okta account should create a new User if one does not exist, otherwise, it will log in as an existing User.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_client_portal.png
  :alt: Client Portal

|br|

.. image:: ../_static/images/oauth-authentication/oauth2_okta_user_login.png
  :alt: User Login Page

|br|

This should also navigate to choose the Okta account you want to sign in with.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_signin.png
  :alt: Okta Sign-in Page

|br|

Choose your account and you should be logged in as a User.

.. image:: ../_static/images/oauth-authentication/oauth2_okta_user_logged_in.png
  :alt: User Logged In
