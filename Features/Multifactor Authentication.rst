.. |br| raw:: html

    <br>

Multifactor Authentication
==========================

Multifactor Authentication, sometimes referred to as Two Factor Authentication, adds an extra layer of authentication set up for Agents.
|br|
when they log into the helpdesk. Once they correctly submit their username and password, they will be required to submit a token to finish logging into the helpdesk.

Agents can configure their Default 2FA settings by going to their profile.

.. image:: ../_static/images/mfa1.png
  :alt: Agent Profile

|br|

.. image:: ../_static/images/mfa2.png
  :alt: Agent Profile 2FA

By default, Agents are not required to set up Multifactor Authentication. An administrator can require Multifactor Authentication by
going to:

Admin Panel | Settings | Agents | Require agents to turn on 2FA

.. image:: ../_static/images/mfa3.png
  :alt: Require Multifactor Authentication

Once enabled, Agents will be required to configure and save their Default 2FA method before accessing the helpdesk.

.. image:: ../_static/images/mfa4.png
  :alt: Configure 2FA

|br|

.. image:: ../_static/images/mfa5.png
  :alt: 2FA Options

|br|

.. image:: ../_static/images/mfa6.png
  :alt: Configure Email 2FA 1

|br|

.. image:: ../_static/images/mfa7.png
  :alt: Configure Email 2FA 2

|br|

.. image:: ../_static/images/mfa8.png
  :alt: Configure 2FA Token

|br|

.. image:: ../_static/images/mfa9.png
  :alt: Configure 2FA Verify Token

Once 2FA has been configured, the Agent must also save the configured method as well.

.. image:: ../_static/images/mfa10.png
  :alt: Choose Default 2FA

|br|

.. image:: ../_static/images/mfa11.png
  :alt: Save Default 2FA

The next time the Agent logs into the helpdesk, they will be prompted to enter a token to finish logging into the helpdesk.

|br|

.. image:: ../_static/images/mfa12.png
  :alt: Agent Login

|br|

.. image:: ../_static/images/mfa13.png
  :alt: Agent Verify Token

|br|

.. image:: ../_static/images/mfa14.png
  :alt: Agent Token Email

|br|

.. image:: ../_static/images/mfa15.png
  :alt: Agent Submit Token

An administrator can edit the Email Template sent for the verification token by going to:

Admin Panel | Settings | Agents | Templates | Two Factor Authentication Email

.. image:: ../_static/images/mfa16.png
  :alt: Agent Email Templates

|br|

.. image:: ../_static/images/mfa17.png
  :alt: Two Factor Authentication Email Template

**Note:** The template variable that contains the token is %{otp}

In the event that an Agent becomes locked out of their account, an Administrator can reset their 2FA configuration by going to:

Admin Panel | Agents | click Agent | Reset 2FA

.. image:: ../_static/images/mfa18.png
  :alt: Reset 2FA
