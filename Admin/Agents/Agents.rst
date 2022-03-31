Agents
======

**Admin Panel > Agents > Agents**

.. image:: ../../_static/images/admin_agents_agents.png
  :alt: Agents Tab

Agents are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department. Agents can be given Extended Access to additional departments of the help desk as well as assigned different Roles to those departments; this can be configured in the Access tab of the Agent’s Profile.

**Reset an agent’s password**

If necessary, administrators can manually reset an agent’s password by clicking the Set Password box in the middle of the Account page. This will produce a pop-up box with two options; the first is to send a password reset email to the agent. **Please note**, if the agent has not first set a password post-creation they can not reset said password. The second option for the admin is to uncheck the box which will populate fields to manually set a password for the agent. Once manually set, the admin will need to communicate this to the agent allowing them to log-in; the agent can be forced to reset the password upon logging in by keeping the box checked at the bottom left of the pop-up.

**Status and Settings**

  **Locked:** Agents who are Locked/Disabled are unable to log into the help desk. They will not be visible for assignment or auto assignments. Email alerts will not be sent to disabled agents as well.

  **Administrator:** Agents marked as “Administrators” simply have access to the Admin Panel are able to make global configuration changes to the help desk. All changes are effective moving forward and will not revert to previously configured settings. Agents with access to the Admin Panel can grant additional agents access to this panel for global configurations.

  **Limit ticket access to ONLY assigned tickets:** When this is checked these agents will only see tickets which are directly assigned to them as an agent or a team to which the agent belongs- regardless of department access. Once tickets are set to a status of a closed state, the assignment is released and the agent will lose access to these closed tickets; if the ticket is reopened, the agent could regain access if it is reopened assigned to them.

  **Vacation Mode:** Agents who are on vacation mode are able to log into the help desk but, like Locked/Disabled agents, they will not be visible for assignment or auto assignments and email alerts will not be sent to these agents as well. An agent can manually set themselves to Vacation Mode in their Profile or an agent with access to the Admin Panel. Vacation Mode must be manually enabled as well as disabled.

Agent Access
------------

Agents are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department. Agents can be given Extended Access to additional departments of the help desk as well as assigned different Roles to those departments; this can be configured in the Access tab of the Agent’s Profile.

Fall back to primary role
For agents without department access which are granted access to tickets via Ticket Assignment/Ticket Referral, they will have Primary Role Permissions for tickets if this is checked. Otherwise, Agents will have a view only access to these tickets allowing them to post an internal note only.

**Agent Permissions**

  **Users**

   **Create:** Ability to add new users

   **Edit:** Ability to manage user information

   **Delete:** Ability to delete users

   **Manage Account:** Ability to manage active user accounts

   **User Directory:** Ability to access the user directory

  **Organizations**

   **Create:** Ability to create new organizations

   **Edit:** Ability to manage organizations

   **Delete:** Ability to delete organizations

  **Knowledgebase**

   **FAQ:** Ability to add/update/disable/delete knowledgebase categories and FAQs

  **Miscellaneous**

   **Banlist:** Ability to add/remove emails from banlist via ticket interface

   **Search:** See all tickets in search results, regardless of access

   **Stats:** Ability to view stats of other agents in allowed departments
