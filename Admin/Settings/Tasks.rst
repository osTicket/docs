Task Settings
=============

**Admin Panel > Settings > Tasks**

Settings
--------

**Default Task Number Format:** This setting is used to generate task numbers. Use hash signs (`#`) where digits are to be placed. Any other text in the number format will be preserved.  For example, for six-digit numbers, use ######.

**Default Task Number Sequence:** Choose a sequence from which to derive new task numbers. The system has an incrementing sequence and a random sequence by default. To create a new sequence, click on the Manage tab to the far right of the field.

.. image: ../_static/images/admin_settings_tasks_sequence.png
  :alt: Default Number Sequence

**Default Priority:**  Choose a default Priority for tasks not assigned a priority automatically.

**Attachments:**
Configure settings for files attached to the **Description** field. These settings are used for all new tasks and new messages regardless of the source channel (web portal, email, api, etc.).

.. image: ../_static/images/admin_settings_tasks_attachments.png
  :alt: Attachments

  **Included in the configurations box:**
  **Enabling of Attachments:** This is a global setting pertaining to new tickets created on the client portal or emailed into the help desk. If disabled, tickets will be created but no attachments will be included if sent via email. If the ticket is created on the client portal and attachments are disabled, there will be no attachment field within the Ticket Details unless a custom field is added to the ticket (either on the Ticket Details built in form or a custom form associated with a help topic) to accept attachments.

  **Maximum File Size:** This is the size per attachment that is acceptable when tickets are created or responses are posted. If an attachment exceeds this limit, an internal note will be posted letting the agent know an attachment was not accepted.

  **Attachment File Limitations:** Allows the configuration of specific types of attachments if necessary.

  **Maximum Attachments Allowed by the end-user:** If necessary, the number of files can be limited per upload of attachments.

  **Help Text:**
  Text that will appear under the field to help users and agents creating tickets get a better understanding of the information being gathered.


Alerts & Notices
----------------

There are messages which can be enabled to alert agents of the events in a Task’s lifecycle. These messages templates can be edited in the Admin Panel > Emails > Templates and include:

**New Task Alert:** Alert sent out to Agents when a new task is created.

**New Activity Alert:** Alert sent out to Agents when a new message is appended to an existing task.

**Task Assignment Alert:** Alert sent out to Agents on task assignment.

**Task Transfer Alert:** Alert sent out to Agents on task transfer between Departments.

**Overdue Task Alert:** Alert sent out to Agents when a task becomes overdue based on SLA or Due Date.
