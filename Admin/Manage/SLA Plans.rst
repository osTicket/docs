SLA Plans
=========

**Admin Panel > Manage > SLA (Service Level Agreements)**

Create A New SLA Plan
---------------------

SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.

SLA Plans can be created by going to the Admin Panel > Manage > SLA Plans. Click on the top right of the table to “Add New SLA Plan.”

One configuration to note with each SLA Plan is whether it can be overridden on Department transfer or change of Help Topic by being Transient. Transient SLAs are considered temporary and can be overridden by a non-transient SLA on Department transfer or when its **Help Topic** is changed.

Once created, SLA Plans can be determined for Departments, Ticket Filters, and Help Topics. There is also a System Default SLA Plan which can be chosen by going to Admin Panel > Settings > Tickets.

When a ticket is created internally from the Staff Panel, agents can choose an SLA Plan which will override any other assignments to a Department or Help Topic. Agents can also select a Due Date for the ticket which, if passed, will cause the ticket to become overdue. No SLA plan can override a due date.

If a ticket is created from the Client Interface, the SLA Plan associated with the Help Topic will be in effect unless a Ticket Filter is in place and the criteria is met; then the SLA Plan associated with the Ticket Filter will be in effect.

For tickets created via email, the department that the email address is assigned to will determine the SLA plan of the ticket unless a Ticket Filter is in place and the criteria is met; then the SLA Plan associated with the Ticket Filter will be in effect.

**Admin Panel > Manage > SLA Plans:**

**Service Level Agreements:** SLA Plans can be set by help topic and department to ensure the ticket is CLOSED in the allotted or specified amount of time.

  **Name:**  Plan name to be selected when assigning.

  **Grace Period:**  Amount, in hours, before tickets with this SLA will become overdue if not closed in allotted time.

  **Status:**  Choose Active or Disable for the plan.

  **Transient:** SLA can be overridden on ticket transfer or help topic change; if not transient, the SLA will remain the same as it is assigned on ticket creation.

  **Ticket Overdue Alerts:** This will DISABLE overdue alert notices to staff for tickets assigned this SLA.
