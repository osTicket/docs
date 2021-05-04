.. |br| raw:: html

    <br>

Attachments in S3
=================

The Attachments in S3 plugin allows you to store attachments in Amazon S3 instead of the database.
This can be a good option to use for helpdesks that have a heavy load of attachments that are taking up a lot of storage in the database.

Once the plugin has been installed and enabled, it can be configured by going to:

Admin Panel | Manage | Plugins | Attachments hosted in Amazon S3

.. image:: ../_static/images/as31.png
  :alt: All Plugins

|br|

.. image:: ../_static/images/as32.png
  :alt: Attachments in S3 Configuration

Within the configuration, you will need to provide the S3 Bucket to store files in.

The S3 Folder Path is an optional field that allows you to specify a folder or folder path within the bucket to store files in.

**Note:** If the folder or folder path provided does not already exist in S3, it will be created automatically.

The AWS Region of your bucket can be found in S3 by going to the Bucket and clicking the Properties tab.

.. image:: ../_static/images/as33.png
  :alt: AWS Region

Default ACL for Attachments refers to the permissions you want for the files stored in S3. If you aren't sure which option to choose, you can default to
the properties already configured for the Bucket.

For the Access Information section, you need to specify IAM user credentials for a user that is set up with access to S3.

Once you have successfully configured the plugin, you will be able to have the helpdesk store attachments in the S3 by going to:

Admin Panel | Settings | System | Store Attachments

Change the 'Store Attachments' option to 'S3'

.. image:: ../_static/images/as34.png
  :alt: Store Attachments Setting

Now, when an Attachment is added in the helpdesk, it will be saved in S3.

.. image:: ../_static/images/as36.png
  :alt: Open Ticket With Attachment

|br|

.. image:: ../_static/images/as37.png
  :alt: Ticket With Attachment


If you have access to the database, you'll notice that attachments stored in the filesystem can be found in the ost_file table, where ost_ is your table prefix.
If the attachment is successfully stored in the filesystem, there will be an '3' in the 'bk' column. Files stored in the database have a 'D' in the 'bk column'.

.. image:: ../_static/images/as39.png
  :alt: Attachment in Database

If you have access to the server where the osTicket files are stored, you can see the available backends that can be used by running the following:

:code:`php manage.php file backends`

.. image:: ../_static/images/as313.png
  :alt: Show Backends

You can migrate the files from the database to the filesystem by running the following command in the terminal:

:code:`php manage.php file migrate --backend D --to 3`

Where 'backend' refers to the 'bk' column in the database, 'D' stands for the current backend being used, Database in this case, and '3' stands for the backend you want to switch to
which is S3 in this example.

.. image:: ../_static/images/as310.png
  :alt: Command in Terminal

Once the command has been run, you can look back in the database and you will notice the the bk field now shows '3' for all of the attachments since they have been migrated.

.. image:: ../_static/images/as311.png
  :alt: Command in Terminal
