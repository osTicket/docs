Ticket Filters
==============

**Admin Panel > Manage > Ticket Filters**

How to Create Ticket Filters
----------------------------

Ticket Filters are a set of “If ____, Then____” rules that create auto actions for new tickets based on the criteria set forth in the filter. The rules of the filter are applied only to tickets upon creation specific to how the ticket is created.

You can create Ticket Filters associated with information pulled from the email or ticket, such as a name, email address, organization, etc., and can create an auto-response (if desired) connected with a related Canned Response.


**Admin Panel > Manage >Ticket Filters > Add New Filter:**

Update/Add New Filter Section
-----------------------------

  **Filter Name:** Name given to filter for internal use only

  **Execution Order:**  This is a numeric listing of the order you want the tickets to be filtered. You can choose to stop filtering if the criteria for the filter is met- this is best utilized in determining rejected ticket filters.

  **Filter Status:** Active or Disabled

  **Target:**  This is the source of creation of the ticket or the means by which the ticket was created. This will further specify which tickets the filter will be applied. There are 5 Targets to choose from only one can be chosen.

    **ANY:** Applies filter to any tickets that originated from Web forms, API calls, and emails.

    **Web Forms:** Applies filter to any tickets that originated from the Client Portal.

    **API Calls:** If enabled, any tickets created through the API Feature will be processed for the filter if the filter criteria is met.

    **Emails:**  Tickets created from any/all emails sent to the system to create tickets.

      **Specific Email:** A specific email address in the help desk utilized to create new tickets in the system.


Filter Rules Section
--------------------

Up to 25 rules can be added in the Filter Rules section. If adding more than 4 rules to a filter, configure the actions for the entire filter after adding the first four rules and click “save changes” to view more rule boxes.

The rules criteria selection is from any field available in the ticket including custom forms, fields, lists and list properties.

**Matching Methods:**

  **Match Any versus Match All:** If you would like the filter to match ANY of the rules, and then stop- choose Match Any. If you would like all rules of the filter to be matched- choose Match All.


Filter Action Section
---------------------

**Reject Email:** If this is selected, no ticket will be created, therefore, save changes because all other actions below this action are invalid.

**Use Reply-To Email:** Reply to the specified Reply-To email address in the header of the ticket.

**Ticket Auto-Response:** Disable auto-responses to client if the filter rules are met.

**Attach Canned Response:** Send a canned response to the client if the filter rules are met.

**Set Department:** Auto-Assign to a specific Department if filter rules are met.

**Set Status:** This will determine the ticket status once created if the filter rules are met.

**Set Priority:** Assign priority to ticket when rules are met; this will override assigned department priority

**Set SLA Plans:** Assign SLA plan when rules are met; this will override assigned department SLA

**Auto-Assign To:** Auto-assign to specific Staff or Team when rules are matched.

**Set Help Topic:** Ticket can be assigned a specific help topic, which, if applicable, will also add any custom form associated with that Help Topic.
