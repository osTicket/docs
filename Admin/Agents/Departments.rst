Departments
===========

**Admin Panel > Agents > Departments**

.. image:: ../../_static/images/admin_agents_departments.png
  :alt: Departments Tab

Since tickets are routed through Departments in the help desk, there are many settings that can be set for each Department.

**Department Information:**

  **Parent:**  If nesting departments, this is the Parent Department to nest the department under. Please note: If an agent has access to the Parent Department, they will see the tickets of nested or child departments also, but access does not extend from child departments to Parent Departments.

  **Status:** The status of the department will determine its visibility as well as if tickets can be routed to that department.

    **Active:** The department is available when transferring tickets.

    **Archived:** The department is no longer in use and cannot be selected to transfer any ticket. Also, if tickets in that department are reopened via an End-User response it will create a new ticket referencing the original ticket number and subject line but the department will be the system default.

    **Disabled:** Tickets can no longer be transferred to this department and any tickets set up to be auto routed to this department will now be routed to the default department in the Helpdesk. Closed tickets in this department will reopen if the End-User responds.

  **Name:** Department name as it will be displayed throughout the helpdesk.

  **Type:** Select Private if you wish to mask assignments to this Department in the Client Portal. Additionally, when labeled as Private, the **Department Signature** will not be displayed in email replies. At least one department of the help desk must be Public.

  **SLA:** Service Level Agreement for tickets routed to this Department. This the expected amount of time (in hours) that a ticket is expected to be closed once opened. If the ticket is not closed in the allotted amount of time, it will then be Overdue.

  **Schedule:** Schedule is used by the Service Level Agreement when rendering tickets routed to this Department. This setting takes precedence over System and SLA schedule settings.

  **Manager:** Electively, select a Manager for the departments of the help desk. Managers can be configured to receive special alerts.

  **Ticket Assignment:** Enable this to restrict ticket assignment to include only members of this Department. Department membership can be extended to based on Agent’s Department Access, if **Alerts & Notices Recipients** includes those with department access.

  **Claim on Response:** Check this to **disable** auto-claim on response/reply for this department. Agents can still manually claim unassigned tickets.

  **Reopen Auto Assignment:** Check this to disable auto-assignment of reopened tickets for this department. Otherwise, the Ticket will be auto assigned to the last responding Agent.

**Outgoing Email Settings:**

  **Outgoing Email:** Email Address used when responses are sent to Users when Agents post Responses to Tickets.

  **Template Set:** Email **Template Set** used for Auto-Responses and Alerts & Notices for tickets routed to this Department. Template sets can be cloned and edited for department use in the Admin Panel > Emails > Templates.

**Auto Responder Settings:** This allows you to override the global Autoresponder settings for this Department.

  **New Ticket:** If checked, this will disable the New Ticket Auto-Response sent to the User
  when a new ticket is created and routed to this Department.

  **New Message:** If checked, this will disable the Auto-Response sent to the User to confirm a newly-posted message for tickets in this Department.

  **Auto-Response Email:** Select an email address from which Auto-Responses are sent for this Department; this email would send only auto-response messages, not Agent responses.
