Email Templates
===============

osTicket relies on predefined templates when sending out auto responses, notices and alerts. Each template has a set of variable placeholder as shown below.

Variables
---------

**BASE VARIABLE**

=====================   ===============================
%{ticket.id}            Ticket ID (internal ID)
%{ticket.number}        Ticket number (external ID)
%{ticket.email}         Email Address
%{ticket.name}          Full Name
%{ticket.subject}       Subject
%{ticket.phone}         Phone Number | ext
%{ticket.status}        Status
%{ticket.priority}      Priority
%{ticket.assigned}      Assigned Staff and/or Team
%{ticket.create_date}   Date Created
%{ticket.due_date}      Due Date
%{ticket.close_date}    Date Closed
%{ticket.auth_token}    Auth. Token used for auto-login
%{ticket.client_link}   Client's Ticket View Link
%{ticket.staff_link}    Staff's Ticket View Link
=====================   ===============================

**EXPANDABLE VARIABLES**

================ ======================
%{ticket.dept}   Department
%{ticket.staff}  Assigned/Closing Staff
%{ticket.team}   Assigned/Closing Team
%{ticket.thread} Ticket Thread
%{ticket.topic}  Help topic
%{ticket.user}   Ticket Owner
================ ======================

**OTHER VARIABLES**

============    ================================
%{message}      Incoming Message
%{response}     Outgoing Response
%{comments}     Assign/Transfer Comments
%{note}         Internal Note (expandable)
%{assignee}     Assigned Staff/Team
%{assigner}     Staff Assigning the Ticket
%{signature}    Staff/Dept Signature (selection)
%{url}          osTicket's Base URL (FQDN)
============    ================================

**NEW VARIABLES**

==================================   =======================================
%{ticket.thread.complete}            Thread Correspondance
%{ticket.thread.complete.reversed}   Thread Correspondance in reversed order
==================================   =======================================

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
