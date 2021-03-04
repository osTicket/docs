.. |br| raw:: html

    <br>

Schedules
=========

Setting up a schedule lets you specify hours of operation for your help desk so that Tickets will only be marked overdue during those times.

.. raw:: html

    <div style="position: relative; padding-bottom: 2%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/jaUs4InKXDY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>

Schedules tie into your helpdesk’s SLA, or service level agreement, which is the amount of time given to respond to a ticket that comes into the helpdesk before it is marked overdue.

You can see the SLA’s you have setup by going to

Admin Panel | Manage | SLA

.. image:: ../../_static/images/schedules1.png
  :alt: Manage SLAs

If you assign a Schedule to an SLA, Tickets will only be marked as overdue within the Business Hours specified in that Schedule.

.. image:: ../../_static/images/schedules2.png
  :alt: Assign SLA Schedule

Create a Schedule
-----------------

Let’s take a look at how to create a schedule.

You can create and configure schedules by going to

Admin Panel | Manage | Schedules

.. image:: ../../_static/images/schedules3.png
  :alt: Manage Schedules

We have several schedules set up by default that can be used or reconfigured to meet your own needs.

There are 2 types of Schedules:

- **Business Hours** which are the hours in which your helpdesk operates
- **Holiday Hours** which are special exceptions that should be applied to your normal hours of operation

Business Hours
--------------

First, we’ll go over how to create business hours.

.. image:: ../../_static/images/schedules4.png
  :alt: New Business Hours

For the timezone, we recommend leaving it blank. This will apply the schedule to the default timezone set in the helpdesk. You can, however, force a specific timezone if you wish.

.. image:: ../../_static/images/schedules5.png
  :alt: New Business Hours 2

.. image:: ../../_static/images/schedules6.png
  :alt: New Business Hours 3

Once your schedule is created, you can add entries to it

.. image:: ../../_static/images/schedules7.png
  :alt: New Business Hours Entry

Let’s say your company operates Monday - Friday from 9am to 5pm. To set this up, we can create an entry for weekdays, specifying those times.

.. image:: ../../_static/images/schedules11.png
  :alt: New Business Hours Weekdays

.. image:: ../../_static/images/schedules30.png
  :alt: New Business Hours Weekdays

**Note:** If you need to set up different hours of operation per day, for example, Monday - Thursday 9am to 5pm and Friday 9am to 12pm, you would need to create an entry for each day.

.. image:: ../../_static/images/schedules8.png
  :alt: New Business Hours Entry

.. image:: ../../_static/images/schedules10.png
  :alt: New Business Hours Completed Entries

Holiday Hours
-------------

After you have specified the hours your helpdesk works, you can specify which hours your helpdesk is not in operation by setting up Holiday Hours.

Let’s say that next Monday is a holiday for the company who uses my helpdesk. First, I would need to create the Holiday.

.. image:: ../../_static/images/schedules11.png
  :alt: Create Holiday 1

.. image:: ../../_static/images/schedules12.png
  :alt: Create Holiday 2

.. image:: ../../_static/images/schedules13.png
  :alt: Add Holiday Entry 1

I want this holiday to fall on Monday, March 23rd each year.

.. image:: ../../_static/images/schedules14.png
  :alt: Add Holiday Entry 2

.. image:: ../../_static/images/schedules18.png
  :alt: Save Holiday Entry

Now that I have the holiday set up, I will apply it to the schedule I have created.

.. image:: ../../_static/images/schedules15.png
  :alt: Add Holiday to Schedule 1

.. image:: ../../_static/images/schedules16.png
  :alt: Add Holiday to Schedule 2

.. image:: ../../_static/images/schedules17.png
  :alt: Add Holiday to Schedule 3

Diagnostics
-----------

After you have everything configured, you have the option to look at a diagnostic tool to show what your working schedule will look like.

.. image:: ../../_static/images/schedules19.png
  :alt: Diagnostic 1

.. image:: ../../_static/images/schedules20.png
  :alt: Diagnostic 2

The number of hours you specify will show what you schedule will look like for that number of working hours.

So, if I have 24 hours in the blank, I will see what the next 24 working hours in my helpdesk look like.

As you can see, the schedule shows the holiday we have entered as skipped hours, and it picks up the following day.

.. image:: ../../_static/images/schedules21.png
  :alt: Diagnostic 3

Clone a Schedule
----------------

You also have the ability to clone a schedule using the same dropdown

.. image:: ../../_static/images/schedules22.png
  :alt: Clone 1

.. image:: ../../_static/images/schedules23.png
  :alt: Clone 2

.. image:: ../../_static/images/schedules24.png
  :alt: Clone 3

Now that we have built out the schedule and assigned holidays to it, we can specify where the schedule should be used.

Schedules can be assigned in several places in the helpdesk.

System Default Schedule
-----------------------

You can choose a default schedule for the whole system.

Settings | System

.. image:: ../../_static/images/schedules25.png
  :alt: System Default Schedule

SLA Schedule
------------

SLA’s can be assigned a schedule.

Manage | SLA | click SLA

.. image:: ../../_static/images/schedules26.png
  :alt: SLA Schedule 1

.. image:: ../../_static/images/schedules27.png
  :alt: SLA Schedule 2

Department Schedule
-------------------

Departments can be assigned a schedule as well.

Agents | Departments | choose Department

.. image:: ../../_static/images/schedules28.png
  :alt: Departments Schedule 1

.. image:: ../../_static/images/schedules29.png
  :alt: Departments Schedule 2

If no Schedule is chosen, the SLA’s default Schedule will be assigned.

If the SLA doesn’t have a Schedule specified, the System Default Schedule will be applied.

If your helpdesk doesn’t have a default Schedule chosen, your Tickets will be marked overdue based on the SLA assigned to the Ticket.
