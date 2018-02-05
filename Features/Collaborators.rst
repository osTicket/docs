Collaborators
===================

Collaborators are additional participants that may be included in a ticket’s communications. This document will outline changes that have been made to how this feature works.

New Features:
-------------

#. Add collaborators as well as CC or BCC them when opening a ticket from the Agent Panel.
#. Add collaborators as well as CC or BCC them when replying to a ticket as an agent.
#. Manage collaborators (add, remove, set CC or BCC status).
#. Change the email address where a ticket is sent out from.
#. Add BCC Collaborator responses as internal notes.
#. View recipients that receive a reply from an agent.
#. As an end user, if you have been BCC’d, allow visibility of only the internal notes that you have posted.
#. As an end user, there is now an icon on the ticket list view to determine if you are a collaborator.
#. New Email Template variables.

CC vs BCC:
-----------------------------------

For this feature, any users added as a CC collaborator will receive and be able to respond to tickets in the same way the ticket’s assigned user does. BCC’d collaborators are not visible to the ticket’s user or CC Collaborators, and they are able to communicate privately on a ticket.

Collaborators on Ticket Open:
-----------------------------------

When an agent creates a ticket on behalf of a user, they now have the option to add Collaborators. Checking the box beside ‘Collaborators’ gives Agents the ability to CC or BCC other users when opening a ticket.

.. image:: ../../_static/images/collabs_open_ticket.png
  :alt: Collaborators Open Ticket

Collaborators on Ticket Reply:
-----------------------------------

Similarly, an agent can add collaborators or choose which collaborators receive an email when replying to a ticket. All users listed in CC or BCC will receive an email with the agent’s response. If a user is chosen that was not previously a collaborator on the ticket, they will be added as a collaborator upon sending the message. Collaborators that are removed by clicking the ‘x’ in the left corner of the user’s name will not receive the agent’s response, however, they will still be listed as collaborators for the ticket. To completely remove a Collaborator, the agent must go to ‘Manage Collaborators’.

.. image:: ../../_static/images/collabs_ticket_reply.png
  :alt: Collaborators Ticket Reply

Removing a Collaborator Recipient:

.. image:: ../../_static/images/collabs_remove_recipient.png
  :alt: Remove Collaborator Recipient

Click Ok:

.. image:: ../../_static/images/collabs_confirm_removal.png
  :alt: Collaborator Removal Confirmed

Manage Collaborators:
-----------------------------------

There are two places where an agent can go to manage collaborators. The first is beside the User’s name on the ticket. There is a group icon with the number of collaborators the ticket has.

.. image:: ../../_static/images/collabs_user_manage.png
  :alt: Manage Collaborators Users

The second place is in the drop down menu next to the ticket settings icon. There is an item to ‘Manage Collaborators’.

.. image:: ../../_static/images/collabs_dropdown_manage.png
  :alt: Manage Collaborators Dropdown

After clicking either of these two options, the menu appears to manage the collaborators. The trash can to the far right of the row allows you to remove collaborators from a ticket. You can also add new collaborators as well as change whether the collaborator will be CC’d or BCC’d in communications.

Standard View:

.. image:: ../../_static/images/collabs_standard_view.png
  :alt: Collaborators Standard View

Changing between CC and BCC:

.. image:: ../../_static/images/collabs_switch_type.png
  :alt: Collaborators Change Type

Remove:

.. image:: ../../_static/images/collabs_remove.png
  :alt: Remove Collaborator Completely

Add:

.. image:: ../../_static/images/collabs_add1.png
  :alt: Add Collaborator

.. image:: ../../_static/images/collabs_add2.png
  :alt: Collaborator User Selected

.. image:: ../../_static/images/collabs_add3.png
  :alt: Collaborator Added

***Note:** By default, collaborators are added as CC Collaborators. Once added, the agent can change the Collaborator to be BCC’d by using the dropdown beside the Collaborator’s name.

***Note:** The checkbox to the left of the collaborator’s name indicates if the collaborator is active or inactive. Inactive collaborators will not receive ticket responses.

‘From’ Email:
-----------------------------------

In the past, tickets were always sent out using the email address belonging to the Ticket’s Department. Agents are now able to choose which email address a ticket is sent out from if your system has more than one email configured.

.. image:: ../../_static/images/collabs_from_email.png
  :alt: From Email

By default, tickets are sent out from the email address chosen for the department’s Outgoing Email. The department’s default address can be modified by going to:

**Admin Panel | Agents Tab | Departments | Choose a Department | Outgoing Email**

.. image:: ../../_static/images/collabs_outgoing_email.png
  :alt: Outgoing Email

BCC’d Collaborator Responses:
-----------------------------------

Deciding to BCC a Collaborator means that you do not want the end user to see that this Collaborator is included on the ticket. An agent could decide to include fellow agents in the communication or maybe even an external Collaborator that should receive communications. For this reason, if a BCC Collaborator responds to the ticket, their responses are only visible to agents as an internal communication. Agents are able to differentiate the type of response by looking at the label next to each message.

Cc Response:
.. image:: ../../_static/images/collabs_cc_response.png
  :alt: Cc Response

Bcc Response:
.. image:: ../../_static/images/collabs_bcc_response.png
  :alt: Bcc Response

In rare occasions, a user may create a ticket and Bcc someone in the email sent in for the ticket. If the person that was Bcc’d responds to the email as a ‘Reply All’, they will be added as a Cc collaborator and their message will be seen by the user and all collaborators. If they only reply to the helpdesk, they will be added as a Bcc collaborator and only agents will see their messages.

View Email Recipients:
-----------------------------------

Any time an email is sent out whether it is from the Agent or the User, there is now an option to see who the email was sent out to. This can be done by clicking the drop down arrow beside a ticket thread and selecting ‘View Email Recipients’.

User Response:

.. image:: ../../_static/images/collabs_user_response.png
  :alt: User Response

.. image:: ../../_static/images/collabs_user_recips.png
  :alt: User Recipients

Agent Response:

.. image:: ../../_static/images/collabs_agent_response.png
  :alt: Agent Response

.. image:: ../../_static/images/collabs_agent_recips.png
  :alt: Agent Recipients

BCC Collaborator Visibility:
-----------------------------------

If a user has been BCC’d on a ticket and they log in to view the ticket, they are able to see all of the responses between the Agent and User as well as their own responses to the ticket. All agent internal notes and all responses from other Bcc’d users are hidden from the ticket user and Cc’d collaborators.

Collaborator Icon:
-----------------------------------

When end users log into the system and view the list of tickets they have access to, they will now see an icon beside the ticket name if they are a Collaborator on the ticket. If there is no icon, they are the ticket owner.

.. image:: ../../_static/images/collabs_icon.png
  :alt: Collaborator Icon

Email Template Variables:
-----------------------------------

**1. Ticket Recipients:**

**Format:** %{ticket.recipients}
This variable displays a list of visible/active users that are collaborating on a ticket. The list excludes Bcc’d users so that private collaborators remain hidden.

**2. Poster Type:**

**Format:**  %{note.posterType}
This variable can be used in the ‘New Internal Activity Alert’ template to let the Ticket Owner know if an Agent has posted an internal message or if the poster was one of the Bcc’d Collaborators.

Default Text:
	An agent has logged activity on ticket #{ticket.number}
Using new variable:
	A(n) %{note.posterType} has logged activity on ticket #%{ticket.number}
