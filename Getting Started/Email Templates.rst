Email Templates
===============

osTicket relies on predefined templates when sending out auto responses, notices and alerts. Each template has a set of variable placeholder as shown below.

Variables
---------

**BASE VARIABLE**

=====================   ===============================
%{ticket.id}            Ticket ID (internal ID)
%{ticket.number}        Ticket number (external ID)
%{ticket.email}         Email address
%{ticket.name}          Full name
%{ticket.subject}       Subject
%{ticket.phone}         Phone number | ext
%{ticket.status}        Status
%{ticket.priority}      Priority
%{ticket.assigned}      Assigned staff and/or team
%{ticket.create_date}   Date created
%{ticket.due_date}      Due date
%{ticket.close_date}    Date closed
%{ticket.auth_token}    Auth. token used for auto-login
%{ticket.client_link}   Client's ticket view link
%{ticket.staff_link}    Staff's ticket view link
=====================   ===============================

**EXPANDABLE VARIABLES**

=============== ======================
%{ticket.topic} Help topic
%{ticket.dept}  Department
%{ticket.staff} Assigned/closing staff
%{ticket.team}  Assigned/closing team
=============== ======================

**OTHER VARIABLES**

============    ================================
%{message}      Incoming message
%{response}     Outgoing response
%{comments}     Assign/transfer comments
%{note}         Internal note (expandable)
%{assignee}     Assigned staff/team
%{assigner}     Staff assigning the ticket
%{signature}    Staff/Dept signature (selection)
%{url}          osTicket's base url (FQDN)
============    ================================

Variable Contexts
-----------------

Please note that only known (supported) variables are substituted. Non-base variables depends on the context of template type to which they are used.

#. **New Ticket Auto Response:** Autoresponse sent to user/client on new ticket if enabled. Meant to give the user the ticket ID which can be used to check the status of the ticket.
#. **New Message Auto Response:** Confirmation sent to user when a new message is appended to an existing ticket. This can be emailed or web-based replies.
#. **Over Limit Notice:** Ticket denied notice. This is a one time notice sent when the user has reached the max allowedopen tickets defined in preference section. Reasonable limit helps control spam and possible email flood loops.
#. **Ticket Response/Reply:** Message template used when responding to a ticket or simply alerting the user about a response/answer availability.
#. **New Ticket Alert:** Alert sent to staff on new ticket.
#. **New Message Alert:** Alert sent to staff when user replies to an existing ticket.
#. **New Internal Note Alert:** Alert sent to selected staff ( if enabled) when an internal note is appended to a ticket.
#. **Assigned Ticket Alert:** Alert sent to staff on ticket assignment.
#. **Overdue/Stale Alert:** Alert sent to staff on stale or overdue ticket.
