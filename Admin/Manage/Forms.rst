Forms
=====

**Admin Panel > Manage > Forms**

Creating and Using Forms
------------------------

A great way to customize the help desk to suit your unique use case is to add custom fields to either a built-in form for each ticket created from the Client Portal or internal tickets opened by agents. Included in the Help Desk are Built-In Forms and the ability to create Custom Forms.


Custom Forms
------------

Custom Forms allow you to create a variety of answer fields which are all customizable. Fields can be listed as internal- to be utilized by staff for internal ticket creation or when editing an existing ticket; or required for when the user submits a ticket. These Custom Forms can then be added to Help Topics to help improve workflow by capturing any required information from the user when submitting a ticket.

To assign a Custom Form to a **Help Topic**, go to Admin Panel > Manage > Help Topics > and select desired help topic. In the Forms Tab of the selected Help Topic, choose custom form from the drop down to be added when clients or staff are creating a new ticket. Multiple Custom Forms can be added to each Help Topic but only one of each Custom Form.

Custom Forms can also be amended to a ticket, a user profile or an Organization by utilizing the “More” quick button on the top right corner.


Built-In Forms
--------------

These forms are included on each new ticket that is created by client or staff; regardless of Help Topic selected. Currently, the software ships with Contact Information, Ticket Details, Task Details, Organization Information, and Company Information as Built-in Forms which are included on each new ticket created. We suggest you preview these built-in forms to see the information contained in them. All can be edited to further work with your company’s workflow. Fields which are marked “Required” will show in bold on the ticket form.

  **Contact Information:** This is the information associated with users in your help desk. This information will not be visible along the ticket header- only with the user’s profile if you click on their name on the ticket header. You can also view and edit this information in the User Directory.

  **Company Information:** This is referring to your Help Desk company information and can be pulled into email templates, signatures, or canned responses utilizing the variables.

  **Organizational Information:** You can expand the information you include when creating Organizations in your User Directory. This information will only be visible internally by your Help Desk Agents when they are reviewing the information associated with the Organizations.

  **Ticket Details:** The information in these fields are collected on each ticket created when Users go to your Client Portal and click “Open a New Ticket” or when tickets are created internally by Agents. These fields can be deemed required and/or internal.

  **Task Details:** The information in these fields are collected on each ticket created when Users go to your Client Portal and click “Open a New Ticket” or when tickets are created internally by Agents. These fields can be deemed required and/or internal.

Field Types and their possible configurations include:

**Short Answer:** You can limit the number of characters (including spaces) someone can enter into the field.

  **Config box:**

  **Field Setup-**
    **Size:** Width, in characters, that the field box will appear for data entry.

    **Max Length:**  The maximum amount of characters someone can type in the field (up to 64,000).

    **Validator:** Select from the list of available validators for the information requested in the short answer including:

      IP Address

      Phone

      Email Address

      Number

      Custom (regular expression)

        Regular Expression

    **Validator Error:**  Error message the end-user will see if the information in the field does not match the validator.

    **PlaceHolder:** Text that will appear in the box until the user clicks in the box to input text.

    **Help Text:** Text that will appear under the field to help users and agents creating tickets get a better understanding of the information being gathered.

  **Settings:**

    **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

    **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

    **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

    **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Long Answer:**  Allows users to include a large amount of text in a form. You can configure to limit as necessary.

  **Config box:**

  **Field Setup-**
    **Width (chars):**  Width, in characters the text box will be sized.

    **Height (rows):**  Number of rows the text box will appear in height.

    **Max Length:**  Maximum number of characters allowed to be typed in the box.

    **Allow HTML:** Enable the HTML/Rich Text toolbar for the end-users.

    **Placeholder:**  Text that will appear in the box until the end-user clicks on the box to type text.

    **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

  **Settings:**

    **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

    **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

    **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

    **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Date & Time:** Allows end-users to select a date from the calendar as well as time. Time is formated in Military Time.

    **Config box:**

    **Field Setup-**
      **Time:** Show time selection with date picker.

      **Time Zone Awareness:** Show date/time relative to user's timezone.

      **Earliest:** Choose the earliest date the end-user can select.

      **Latest:**  Choose the latest date an end-user can select.

      **Allow Future Dates:** Check to allow the end-user to choose a date in the future

      **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

    **Settings:**

      **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

      **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

      **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

      **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

      **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Phone Number:** To enter a phone number from end-user; can be between 7-16 digits.

      **Config box:**

      **Field Setup-**
      **Extension:**  Check the box for the end-user to be able to input an extension into a separate field than the phone number.

      **Minimum Length:** Fewest digits allowed for a valid phone number.

      **Display Format:** Currently, only format available is US.

      **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

      **Settings:**

        **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

        **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

        **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

        **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

        **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Check Box:** Can be utilized in questions requiring only one answer.

        **Config box:**

        **Field Setup-**
        **Description:** Text to be shown inline with checkbox widget.

        **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

        **Settings:**

          **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

          **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

          **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

          **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

          **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Choices:** Allows you to enter items that are chosen by end-user in a dropdown box

  **Config box:**

    **Choices:** Enter the list choices (one per line) for end-users to select from. To protect against spelling changes, “specify key:value names” to preserve entries if the list item names change. For example, in the list below, the key is the number before the value name:
    1: Apple
    2: Orange
    3: Banana

    **Default:** Enter the key value for the item in the choices that the system will default to when the ticket is being created. end-users can select a different value from the list if that is not the choice for them.

    **Prompt:** Leading text shown on the drop down field for the end-user if there is no default choice entered in the configurations.

    **Multi-select:** Enable end-users to choose more than one choice from the drop down box

    **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

  **Settings:**

    **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

    **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

    **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

    **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Section Break:** This feature allows distinction of form sections by adding a break with a title. The field label will show up in a grey box that has extended the width of the form.

  **Config box:**

    **Field Setup-**
    **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

  **Settings:**

    **Enabled:** This field can be disabled which will remove it from the form for new entries, but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

**Information:** This field does not require input from the end-user nor the agent when creating a ticket. It is simply a way to communicate some sort of information.

  **Config box:**

    **Field Setup-**
    **Content:** Type your message here in a lighter, italicized font.

    **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

  **Settings:**

    **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

    **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

    **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

    **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**File Upload:** Allows End-Users to include attachments in association with custom fields other than the Issue Details field located in the Ticket Details form. Please note; attachments can be required for ticket creation if this field is marked as required.

  **Config box:**

    **Field Setup-**
    **Max File Size:** Choose maximum size of a single file uploaded to this field.

    **Restrict by File Type:** Optionally, choose acceptable file types.

    **Additional File Type Filters:** Optionally, enter comma-separated list of additional file types, by extension. (e.g .doc, .pdf)

    **Max Files:** Enter the maximum number of files users can upload per response.

    **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

  **Settings:**

    **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

    **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

    **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

    **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Built-In:**
  **Priority Level:** (Low, Normal, High, Emergency) If selecting this as a required field, it will override the priority level of the Help Topic & Department.

  **Department:** This field will populate the public Departments of the Help Desk

  **Assignee:** This field will populate a list of all Agents of the Help Desk.

  **Settings:**

    **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

    **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

    **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

    **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

    **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.

**Custom Lists:**
    You must first CREATE a custom List in Admin > Manage > Lists before it will show up in the “Type” of field.

    **Config box:**

      **Field Setup-**
      **Multi-select:** Enable end-users to choose more than one choice from the drop down box

      **Widget:** Select the type of List you would like the field to be: Typeahead, Dropdown, or Text Entry.

      **Prompt:** Leading text shown on the drop down field for the end-user if there is no default choice entered in the configurations.

      **Default:** Select the default value for the field from the list items in the drop down;  the system will default to this choice when the ticket is being created. end-users can select a different value from the list if that is not the choice for them.

      **Help Text:** Text that will appear under the field to help your end-users and agents creating tickets get a better understanding of the information being gathered.

    **Settings:**

      **Enabled:** This field can be disabled, which will remove it from the form for new entries but will preserve the data on all current entries.

      **Visible:** Making fields visible allows agents and end-users to view and create information in this field.

      **Required:** Determines if information is necessary for new entries to be created All required fields must have valid data.

      **Editable:** Fields marked editable allow agents and end-users who are the ticket owner to update the content of this field after the form entry has been created.

      **Require Entry:** Optionally, this field can prevent closing a thread until it has valid data.
