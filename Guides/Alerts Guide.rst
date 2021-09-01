Alerts Guide
============

Autoresponder
-------------

*Admin Panel > Settings > Tickets > Autoresponder.*

Auto-responses are messages which can be enabled to alert end-Users of the events in a Ticket’s lifecycle.

**New Ticket:** Enable this to send an auto response to the User on new ticket creation.

**New Ticket By Agent:** Notice sent when an Agent creates a ticket on behalf of the User. Agents can override this when creating new tickets by selecting recipients in the drop down. Options include only notifying the ticket owner, all participants or not sending an alert to either. .

**New Message:**

**Submitter:** Confirmation notice sent when a new message is appended to an existing ticket. Submitters can be any participant on a ticket including a collaborator or the owner of the ticket.

**Participant:** Broadcast messages received from message submitter to all other participants (collaborators or owner) on the ticket.

**Overlimit Notice:** Ticket denied notice sent to User on Maximum Open Tickets violation. Configuration for this limit is in the Admin Panel > Settings > User.

Alerts and Notices
------------------

*Admin Panel > Settings > Tickets > Alerts and Notices.*

Alerts and Notices are messages which can be enabled to alert agents of the events in a Ticket’s lifecycle. These message templates can be edited in the Admin Panel > Emails > Templates.

**New Ticket Alert:** Alert sent out to Agents when a new ticket is created. This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-1.png
  :alt: New Ticket

New Ticket Alert for **Admin Email** is sent to the listed email for each ticket created in the help desk, regardless of the department it is routed to. This template is not accessible nor editable and can only be globally enabled or disabled. The Admin Email can be set in the Admin Panel > Emails > Settings tab.

New Ticket Alert for **Department Manager** will be sent to the Department Manager, if set, for the Department the tickets routed to; this will be the New Ticket Alert template message. If the Department Manager is also a Department Member, only one email will be sent to this agent. Note, an agent does not have to have access to this department to be selected as the Manager.

New Ticket Alert for **Department Members** is sent to the Agents with access to the Department the ticket is routed to when the ticket is created so long as the ticket is not automatically assigned to a specific Agent or Team. (If assigned, no New Ticket Alert will be sent; instead, the Assignment Alert is sent to the Assigned Agent/Team as enabled in the Assignment Alert section.) By Department, you can determine the agents with access to the ticket - Primary Members and/or Extended Access Members - to receive the alert.

New Ticket Alert for **Organization Account Manager** is sent to the agent or team of agents selected as the Organization Account Manager in the Agent Panel > Users Tab > Organizations Tab > Select Organization > Select Organization name in blue > Settings Tab > Account Manager.

**New Message Alert:** Alert sent out to Agents when a new message from the User is appended to an existing ticket. This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-2.png
  :alt: New Message

New Message Alert for **Last Respondent** is sent to the last responding agent when a new message from the end user is appended to the ticket; Regardless of ticket assignment.

New Message Alert for **Assigned Agent/Team** is sent to the assigned agent or team of agents when a message is appended to a ticket from an end user. This is sent to the agents as long as there is no response from any Agent on the ticket. If there is a response from an agent, only the responding agent will receive the New Message Alert if that alert in this section is enabled.

New Message Alert for **Department Manager** is sent to the Department Manager, if set, in the department the ticket is routed when a new message is received from the end users. This is only sent to the Department Manager if there is no agent or team assigned to the ticket and there is no response from an agent on the ticket or neither of the previously mentioned alerts are enabled in this section.

New Message Alert for **Organization Manager** is sent to the Agent or Team of agents set as the Organization Manager in the Agent Panel > User > Organization > Settings. This is sent to the Organization Manager regardless of the last responding agent or assigned agent.

**New Internal Activity Alert:** Alert sent out to Agents when internal activity such as an internal note or an agent reply is appended to a ticket.This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-3.png
  :alt: New Activity

Internal Activity Alert for the **Last Respondent** is sent to the last responding agent for activity on a ticket such as an internal note or another agent’s response to a ticket.

Internal Activity Alert for the **Assigned Agent/Team** is sent to the assigned agent or team if there is no response from another agent posted on the ticket or the alert for last respondent is not enabled.

Internal Activity Alert for the **Department Manager** is sent to the Department Manager, if set, for the Department, and the Last Respondent and Assigned Agent/Team is not listed or the alerts are not enabled.

**Ticket Assignment Alert:** Alert sent out to Agents on ticket assignment.
	This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-4.png
  :alt: New Assignment

Ticket Assignment Alert for **Assigned Agent** is sent only to the agent the ticket is being assigned to.

Ticket Assignment Alert for **Team Lead** is sent to the Agent set as the Team Lead if designated at the Team level

Ticket Assignment Alert for **Team Members** is sent to all team members when a ticket is assigned to the team.


**Ticket Transfer Alert:** Alert sent out to Agents on ticket transfer between Departments.
 This Alert is sent to all Agents with Primary + Extended Department Access (if enabled at Department level) Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-5.png
  :alt: New Transfer

Ticket Transfer Alert for **Assigned Agent/Team** is sent to the current Assigned Agent/Team of agents of the ticket when the ticket is transferred to a new department.

Ticket Transfer Alert for **Department Manager** is sent to the Department Manager (if set at the department level) of the department the ticket is being transferred to.

Ticket Transfer for **Department Members** is sent to all Agents with access (Primary or Extended) to the Department the ticket is being transferred to.

**Overdue Ticket Alert:** Alert sent out to Agents when a ticket becomes overdue based on SLA or Due Date. This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-6.png
  :alt: Overdue Ticket

Overdue Ticket Alert for **Assigned Agent/Team** is sent to the current Assigned Agent/Team of agents of the ticket when the ticket becomes overdue (by passing the ticket’s SLA).

Overdue Ticket Alert for **Department Manager** is sent to the Department Manager (if set at the department level) of the department when the ticket becomes overdue (by passing the ticket’s SLA).

Overdue Ticket Alert for **Department Members** is sent to all Agents with access (Primary or Extended) to the Department when the ticket becomes overdue (by passing the ticket’s SLA).

**System Alerts:** Significant system events that are sent out to the Administrator. Depending on the configured Log Level, the events are also made available in the System Logs

.. image:: ../../_static/images/alerts-guide-1.png
  :alt: System Alert

**Parent/Child Department affect on Alerts/Notices**

*Agents with access to the Parent Department have access to child department tickets by default with parent department role permissions*

*Agents can have primary access to the Parent Department or Extended Access to the Parent  Department and still have access to child department tickets with the set of permissions associated with the department.*

**Task Alerts and Notices**

*Admin Panel > Settings > Tasks > Alerts and Notices Tab.*

There are messages which can be enabled to alert agents of the events in a Task’s lifecycle. These messages templates can be edited in the Admin Panel > Emails > Templates and include:

**New Task Alert:** Alert sent out to Agents when a new task is created. This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-8.png
  :alt: Task Alert

**New Activity Alert:** Alert sent out to Agents when a new message is appended to an existing task. This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-9.png
  :alt: Activity Alert

**Task Assignment Alert:** Alert sent out to Agents on task assignment. This Alert is sent to all members enabled; Duplicate alerts are not sent out.

.. image:: ../../_static/images/alerts-guide-10.png
  :alt: Assignment Alert

Disabling Alerts
----------------

**Autoresponder:**

You can manually disable Autoresponder Alerts at the Email level, Help Topic level, Department level, or with the use of Ticket Filters:

**Email**

You can disable Autoresponders for certain email addresses by going to Admin Panel > Emails > Select an Email Address > locate ‘Auto-Response’ > check the box to disable auto-responses and save changes.

.. image:: ../../_static/images/alerts-guide-11.png
  :alt: Disable Autoresponder

**Help Topics**

Help Topics help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket. Help Topics are located at Admin Panel > Manage Tab > Help Topics. Select a Topic, select the New Ticket Options Tab > locate Auto-Response > Check the box and save changes to disable Autoresponses for this Help Topic.

*See here for additional details on Help Topics.*

.. image:: ../../_static/images/alerts-guide-12.png
  :alt: Disable Help Topic Autoresponder

**Departments**

Tickets are routed through Departments in the help desk, there are many settings that can be set for each Department. Departments are located at Admin Panel > Agents Tab > Departments. Select a Department > locate Autoresponder Settings:
New Ticket: Check this box to disable the Auto-Response sent to the User when a new ticket is created and routed to this Department.
New Message: Check the box to disable the Auto-Response sent to the User to confirm a newly posted message for tickets in this Department.

*See here for additional details on Departments.*

.. image:: ../../_static/images/alerts-guide-13.png
  :alt: Disable Departments Autoresponder

**Ticket Filters**

Ticket Filters are a set of “If ____, Then____'' rules that create auto actions for new tickets based on the criteria set forth in the filter. The rules of the filter are applied only to tickets upon creation specific to how the ticket is created. Ticket filters are located at Admin Panel > Manage Tab > Filters. Within the Filter Actions Tab there is an option to select ‘Disable auto response’.

*See here for additional details on Ticket Filters.*

.. image:: ../../_static/images/alerts-guide-14.png
  :alt: Disable Ticket Filter Autoresponder

**Alerts and Notices:**

You can manually disable Alerts and Notices at the Department level and Agent level. You can also disable assignment alerts at the Team level.

**Department Level**

*Admin Panel > Agents Tab > Departments*

You can configure the recipients of Alerts and Notices at the Department level by locating the ‘Alerts and Notices’ section:

.. image:: ../../_static/images/alerts-guide-15.png
  :alt: Department Alerts and Notices

**Department and Extended Access Members**

Enable alerts for all Primary and Extended Access Members in this Department; full list of Agent’s with access can be seen in the Access tab of the Department

**Department Members only**

Enable alerts for only Agents who have this Department set as their Primary Department; this will included agents in the Top section of the Access tab of the help desk.

**Admin Email Only**

Only send Alerts and Notices to the system Administrator (this configuration is set at Admin Panel > Emails > Settings > Admin Email.)

**No One (Disable Alerts and Notices)**
Disable Alerts and Notices for all Agents in this Department.

**Agent Level**

*Admin Panel > Agents Tab*

You can disable Alerts at the Agent level for any Extended Access Departments by selecting an Agent, then selecting the Access Tab. Locate the Extended Access Departments and un-check the box for Alerts to disable Alerts for a Department, then save changes.

.. image:: ../../_static/images/alerts-guide-16.png
  :alt: Disable Alerts and Notices

**Primary Departments**

You can not disable Alerts specifically for an Agent’s Primary Department. If you want to disable all Alerts for a certain Agent(s), you can create a new Department and disable Alerts for the entire Department (Admin Panel > Agents Tab > Departments.)

.. image:: ../../_static/images/alerts-guide-17.png
  :alt: Disable Primary Department Alerts One


.. image:: ../../_static/images/alerts-guide-18.png
    :alt: Disable Primary Department Alerts Two

Next, you will set this department as the Agent’s Primary Department (Admin Panel > Agents Tab > Agent).

.. image:: ../../_static/images/alerts-guide-19.png
  :alt: Disable Primary Department Alerts Three

Once complete, be sure to add the Agent’s original Primary Department to the Extended access section so that they maintain access to the Department; Also uncheck the box for Alerts to this Department and save changes.)

.. image:: ../../_static/images/alerts-guide-20.png
  :alt: Disable Primary Department Alerts Four

**Assignment alert for teams**

*Admin panel > Agents Tab > Teams.*

You can disable the Assignment alert at the Team level by selecting a Team and locating the Assignment Alert; Check the box to disable alerts for this Team and save changes.

.. image:: ../../_static/images/alerts-guide-21.png
  :alt: Disable Assignment Alert

Editing Template Messages
-------------------------

**Autoresponder Messages**

Autoresponder template messages are located at Admin Panel > Emails Tab > Templates; Select a Template Set to start editing. The ‘Ticket End-User Email Templates’ are the templates associated with Autoresponder messages sent to end Users.

Start editing them by selecting a template message that you would like to edit. Once selecting a message, you can edit the entire template message, including the subject line.

.. image:: ../../_static/images/alerts-guide-22.png
  :alt: Edit Template Autoresponder

**Alerts and Notices Messages**

Alerts and Notices template messages are located at the same place, Admin Panel > Emails Tab > Templates; Select a Template Set to start editing. The ‘Ticket Agent Email Templates’ are the templates associated with Alerts and Notices messages sent to Agents.

.. image:: ../../_static/images/alerts-guide-23.png
  :alt: Edit Template Alerts and Notices

**Task Alerts**

Task Alert template messages are located at the same place, Admin Panel > Emails Tab > Templates; Select a Template Set to start editing. The ‘Task Email Templates’ are the templates associated with Task messages sent to Agents.

.. image:: ../../_static/images/alerts-guide-24.png
  :alt: Edit Template Task Alerts

*Note: The entire set of email templates can be cloned for use and assigned to a specific Department of the Help Desk. This is especially useful if the messages need to be different for tickets assigned to the Department.*

**User Account Message Templates**

There are additional User Template Messages located Admin Panel > Settings > Users > Templates Tab. These template messages are specific to the Authentication and Registration of Users.

.. image:: ../../_static/images/alerts-guide-25.png
  :alt: User Account Templates

**Agent Account Message Templates**

There are additional Agent Template Messages located Admin Panel > Settings > Agents > Templates Tab. These template messages are specific to the Authentication and Registration of Agents.

.. image:: ../../_static/images/alerts-guide-26.png
  :alt: Agent Account Templates

**Variables within Templates**

You will notice variables in Template Messages:

.. image:: ../../_static/images/alerts-guide-27.png
  :alt: Variables in Templates One

Variables automatically pull information (if available) from a submitted ticket. You can use the built-in Variables available, as well as create your own custom variables, specific to your custom fields (on Forms).

Variables are added to a template message by typing %{

.. image:: ../../_static/images/alerts-guide-28.png
  :alt: Variables in Templates Two

From there variables are displayed to choose from, or you can manually enter a custom variable set within your Forms.

.. image:: ../../_static/images/alerts-guide-29.png
  :alt: Variables in Templates Three

  .. image:: ../../_static/images/alerts-guide-30.png
    :alt: Variables in Templates Four

**Built-In Variables**

Within each email template there is a Supported Variables option in the upper right corner that will provide a partial list of built-in variables available. As the forms are built out to contain additional fields there will be more variables available to be used in the email templates and canned responses.

.. image:: ../../_static/images/alerts-guide-31.png
  :alt: Built In Variables

**Creating Custom Variables**

You can create your own custom variables, specific to custom fields on your Forms.

Forms are located at Admin Panel > Manage Tab > Forms. Start by selecting the Form that you would like to edit:

.. image:: ../../_static/images/alerts-guide-32.png
  :alt: Custom Variables One

Next, you will either add a new custom field, or locate one that’s already been added by you previously. In the Variable column of the field you will add a custom name for the variable. You can use both letters and numbers in variables, and variables should have no spacing between words. This variable can later be included in Email Templates or Canned Responses by typing %{ticket.customvariablename}.

.. image:: ../../_static/images/alerts-guide-33.png
  :alt: Custom Variables Two

.. image:: ../../_static/images/alerts-guide-34.png
  :alt: Custom Variables Three

If you add a variable to a template and receive the above error message, please note this does not mean the variable is incorrect. This message is alerting the variable may not be value for all instances when the template message is sent out.

*Note: Variables can also be used in Canned Responses (located at Agent Panel > Knowledgebase Tab > Canned Responses.*
