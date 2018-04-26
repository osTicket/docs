.. |br| raw:: html

    <br>

Dashboard
=========

**Agent Panel > Dashboard > Dashboard**

.. image:: ../../_static/images/agent_dashboard_dashboard.png
  :alt: Dashboard Tab

Meant to be a historical marker of the metadata in your help desk, the Dashboard will give you an overview of tickets in your help desk. The data can be filtered by date as well as Departments, Help Topics, and Agents. This data can also be exported into a CSV file.

**Opened**
|br|
Tickets that were originally opened having the Department or Help Topic on the ticket. When a ticket is created, one item will be added to Opened. For the Agents tab, the Opened column reports how many tickets an agent has manually opened on behalf of a User.

**Assigned**
|br|
Tickets that have been assigned to either an Agent or a Team while also being in the Department or Help Topic listed in the column, or tickets that were assigned to the Agent listed in the column, within the timeframe chosen. The number reflects tickets that are manually assigned to agents or teams, claimed tickets, tickets assigned from ticket filters, tickets assigned based on help topics, and tickets assigned based on user organizations. The number does not reflect tickets where an agent is automatically assigned to a ticket that they they have responded to. Note that if the ticket was assigned to a Team, the report numbers for Agents will not change, even if they are in the team selected.Tickets can be auto-assigned to certain departments and/or agent based on your set up of emails and filters. Tickets can also be assigned internally to other agent/departments. The system tracks each time the ticket is assigned. The colored circles signify the same as above.

**Overdue**
|br|
Tickets that have been marked ‘Overdue’ by the system while having the Department, Help Topic, or Agent on the ticket as well, within the timeframe chosen. Tickets are marked Overdue when they have violated the SLA Plan to which they belonged, causing them to have a status of ‘Open’ past their Due Date

**Closed**
|br|
The number of Tickets in the Department that are currently in the Closed status while having the Department, Help Topic, or Agent on that ticket, within the timeframe chosen. If the ticket is reopened, the number of closed tickets decreases by 1 and the number of Reopened tickets for the department increases by 1.

Tickets can be closed three ways:

  **A.** Go to the ticket listing page, highlight the selected ticket by checking the box on the far left side of the screen. Once the ticket(s) are selected, scroll to the bottom of the page and click on the "close" button in the middle. A pop-up box will appear to ask about closing the selected tickets. Press "Yes" to continue to close the tickets.

  **B.** A ticket can be closed when clicking on the ticket to view the contents of the ticket- this will not send a notification to the sender. At the top right of the ticket screen, there will be buttons including "close". When pressed, a dialogue box will pop-up asking for internal documentation of why the ticket is being closed. Although not required to close the ticket, it is highly recommended.

  **C.** A ticket can also be closed under the "Post Internal Note" tab at the bottom of a ticket. In order to close a ticket in this manner, you must include an internal note then change the "Ticket Status" for that ticket to "closed."

**Reopened**
|br|
The total number of times a ticket was Reopened while having the Department, Help Topic, or Agent listed for the ticket within the timeframe chosen. If a Closed Ticket’s status is changed from Closed to Open, an item is added to Reopened and removed from Closed.

Tickets can be reopened in two ways:

  **A.** A customer can respond to a ticket that agent has closed internally.

  **B.** Select and click on a "closed" ticket > (scroll to the bottom of the ticket ) > Post Internal Note > Change Ticket status.

**Deleted**
|br|
The amount of tickets that have been deleted while having the Department, Help Topic, or Agent listed for the ticket within the timeframe chosen.

Service and Response Time calculate the values for the Departments, Help Topics, or Agents based on what is currently on a ticket. These values are calculated in hours with decimals representing minutes. In order to convert the decimals to minutes, you should multiply the decimal by sixty.

**Service Time**
|br|
Refers to the duration of time that begins at the opening of a ticket and ends when the ticket is closed without being reopened again. The Service Time column measures the average Service Time per ticket, in hours, within the specified date span.

**Response Time**
|br|
Shows an average of the number of hours between when a user posted a message on a ticket and when an agent responded/replied to the customer.
