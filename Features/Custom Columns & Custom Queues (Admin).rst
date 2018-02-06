Custom Columns & Custom Queues (Admin)
======================================

What is a Custom Queue?
-----------------------

A custom queue is a view of tickets based on a custom criteria that you specify. It allows you to create your own personal views of tickets and specify what information you would like to see. 

What is a Custom Column?
------------------------

A custom column is an additional field that is not displayed initially when viewing the ticket tab. Using custom columns allows you to include these fields in the ticket list.


Before adding custom columns:

.. image:: ../../_static/images/cccc_before_adding.png
  :alt: Before Adding Custom Columns

After adding custom columns:

.. image:: ../../_static/images/cccc_after_adding.png
  :alt: After Adding Custom Columns

How can I add a queue that everyone can see?
--------------------------------------------

Admin Panel | Settings Tab | Tickets | Queues Tab | Add New Queue

.. image:: ../../_static/images/cccc_add_global_queue.png
  :alt: Add Global Queue

From here, you can configure the new queue by selecting the criteria of tickets for the queue: 

.. image:: ../../_static/images/cccc_configure_global_queue.png
  :alt: Configure Global Queue

For this example, I chose to create a queue for the Support Department.

Once the queue is created:

.. image:: ../../_static/images/cccc_after_global_queue.png
  :alt: After Global Queue

Where can I edit the default columns and queues?
------------------------------------------------

There are two places where you can edit the default columns and queues:

1. Admin Panel | Settings | Tickets | Queues 

.. image:: ../../_static/images/cccc_edit_default_queues.png
  :alt: Edit Default Queues

2. By simply clicking on the queue, selecting the Settings button that appears beside the title, and choosing Edit.

.. image:: ../../_static/images/cccc_edit_queue_button.png
  :alt: Edit Queue Button

How do I add more columns to a queue?
-------------------------------------

Admin Panel | Settings | Tickets | Queues 

.. image:: ../../_static/images/cccc_edit_default_queues.png
  :alt: Add More Columns To Queue

From there, you will need to select the queue you want to add columns to. In this example, I will select the Open queue.

.. image:: ../../_static/images/cccc_open_queue.png
  :alt: Open Queue

Next, you should select the 'Columns' tab.

.. image:: ../../_static/images/cccc_columns_tab.png
  :alt: Columns Tab

Within the 'Columns' tab, you can select fields to be added as columns, edit the order in which fields show up by dragging the rows, and choose which fields should have the option to be sorted.

Additionally, clicking the 'Config' button beside a field allows you to:

1. Determine how ticket data is displayed

For example, what is shown when hovering over a link or what format dates display as.

.. image:: ../../_static/images/cccc_queue_column_manage.png
  :alt: Queue Column Manage

.. image:: ../../_static/images/cccc_queue_column_manage2.png
  :alt: Queue Column Manage 2

**Note:** Primary and Secondary Data Source refer to the field's data that will show up in a column. Secondary Data Source allows you to choose an alternative field's data to display if the Primary Data Source is not populated.

2. Add an annotation to show up beside specified fields

.. image:: ../../_static/images/cccc_column_annotation.png
  :alt: Column Annotation

An annotation is a small icon that represents more information about a field. For example, the annotation for thread count displays as a chat icon with the number of responses included on a ticket

.. image:: ../../_static/images/cccc_annotation_preview.png
  :alt: Annotation Preview

3. Add (or modify) conditional styling

**Add**

.. image:: ../../_static/images/cccc_add_column_conditions.png
  :alt: Add Column Conditions

**Modify**

.. image:: ../../_static/images/cccc_modify_column_conditions.png
  :alt: Modify Column Conditions

Do custom queues support conditional styling?
---------------------------------------------

There is a feature to add style to queues. These settings can be found by going to:
Admin Panel | Settings | Tickets | Queues

.. image:: ../../_static/images/cccc_edit_default_queues.png
  :alt: Add Styling To Queue

From there, you will need to select the queue you want to add conditional styling to. In this example, I will select the Open queue.

.. image:: ../../_static/images/cccc_open_queue.png
  :alt: Open Queue

Once you select a queue, you should select the 'Conditions' tab where you are able to specify what styling you want and under which criteria. Many options are included to manipulate the color, font style, and text of ticket records.

**Before Adding Conditions:**

.. image:: ../../_static/images/cccc_before_adding_conditions.png
  :alt: Before Adding Conditions

**After adding conditions:**

.. image:: ../../_static/images/cccc_after_adding_conditions.png
  :alt: After Adding Conditions

Once you save a style, you can click the preview tab to see how it looks.

.. image:: ../../_static/images/cccc_queue_styling_saved.png
  :alt: Queue Styling Saved

Adding conditions this way will apply the style to the whole row, as shown above.

If you decide that you want to discard the styling, you can do so by clicking the trash can beside the style.

.. image:: ../../_static/images/cccc_after_adding_conditions.png
  :alt: Delete Style Button

**Additionally, you can add conditional styling to only one field specified.**
To do this, select the Columns tab within the queue you are adding style to.

.. image:: ../../_static/images/cccc_columns_tab.png
  :alt: Columns Tab

Click the 'Config' button for the column to add style to it and then select the 'Conditions' tab.

.. image:: ../../_static/images/cccc_conditions_tab.png
  :alt: Conditions Tab

In this example, I have chosen to add a background color to Departments with the name 'Support'

Once saved, tickets where the Department is 'Support' will have the style added to only the Department column.

.. image:: ../../_static/images/cccc_style_added.png
  :alt: Style Added

How can I customize how tickets are sorted in queues?
-----------------------------------------------------

Sorting options can be found by going to: 
Admin Panel | Settings | Tickets | Queues 

.. image:: ../../_static/images/cccc_edit_default_queues.png
  :alt: Customize Ticket Sorting

From there, you will need to select the queue you want to add column sorting to. In this example, I have selected the Open queue.

.. image:: ../../_static/images/cccc_open_queue.png
  :alt: Open Queue

There are two ways to control how tickets are sorted, and both options can be found from this menu. 

1. By enabling column sort which will let you sort by a column that is clicked

Selecting the 'Columns' tab lets you specify which columns should be sortable by placing a check in the sortable box.

.. image:: ../../_static/images/cccc_columns_tab.png
  :alt: Columns Tab

2. Specifying the dropdown sort options. These settings can be found by going to:

Selecting the 'Sort' tab allows you to specify what sort filters you would like to see in the sort dropdown.

.. image:: ../../_static/images/cccc_queue_sort.png
  :alt: Queue Sort

Once saved, you can see your filters by going to tickets and clicking on the Sort dropdown

.. image:: ../../_static/images/cccc_sort_dropdown.png
  :alt: Sort Dropdown

What is the Parent Queue?
-------------------------

The parent queue is used to determine which column a queue falls under.

.. image:: ../../_static/images/cccc_parent_queue.png
  :alt: Parent Queue

In this example, Cloned Queue, Unanswered, Unassigned, and My Tickets have 'Open' as the Parent Queue.

.. image:: ../../_static/images/cccc_open_parent_queue.png
  :alt: Open Parent Queue

When viewing the 'Open' tab, each of these queues are visible.

.. image:: ../../_static/images/cccc_open_child_queues.png
  :alt: Open Child Queues

What are Quick Filters?
-----------------------

When editing a queue, there is an option to add a Quick Filter. This adds an option at the top of the page to quickly filter by a specified field. 

.. image:: ../../_static/images/cccc_quick_filter.png
  :alt: Quick Filter

In this example, I will add a quick filter for the Department.

.. image:: ../../_static/images/cccc_add_quick_filter.png
  :alt: Add Quick Filter

Now, when I view the Open Tickets queue, I can filter tickets by each Department I have access to.

.. image:: ../../_static/images/cccc_quick_filter_dropdown.png
  :alt: Quick Filter Dropdown

If I click on 'Sales', only tickets in that Department will be shown.

.. image:: ../../_static/images/cccc_sales_filter.png
  :alt: Sales Filter

What does the Default Sorting option do?
----------------------------------------

When editing a queue, there is an option to choose the Default Sorting. This automatically chooses which sorting option agents will see by default.

.. image:: ../../_static/images/cccc_quick_filter.png
  :alt: Default Sorting

By default, no sort is chosen.

.. image:: ../../_static/images/cccc_default_no_sort.png
  :alt: No Sorting Default

Update sort:

.. image:: ../../_static/images/cccc_update_default_sort.png
  :alt: Update Default Sort

Once changed:

.. image:: ../../_static/images/cccc_default_sort_changed.png
  :alt: Default Sort Changed
