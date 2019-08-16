Upgrade and Migration
=====================

Before embarking on an upgrade or a migration mission, it is extremely important that you backup your website's database and files. We also recommend that you take the system offline momentarily during the process. While we try to ensure that the upgrade process is straightforward and painless, we can't guarantee it will be the case for every user. For this reason it is crucial that users take precautions in case of any problems. If the thought of upgrading your installation gives you the shakes then feel free to `contact us for help <https://osticket.com/contact-us/>`_.

Upgrade
-------

From time to time it will be necessary to upgrade your osTicket installation to the latest version, either to fix bugs or gain new features. Starting with version 1.6, osTicket is a complete rewrite with new database schema and code base making it hard to simply upgrade from previous versions.

#. Only previous versions from version 1.6 RC1 can be upgraded to the current version.
#. If your osTicket version is older than 1.6, you need to look into migration instead.

Our objectives is to make upgrading from an earlier release as painless as possible going forward and support migration from discontinued versions. we are working with `osTicket community <https://forum.osticket.com/>`_ on the best way to upgrade or/and import data from previous versions including 3rd party helpdesk systems.

Uploading Files
---------------

After you have successfully downloaded the osTicket package to your computer you will need to prepare the files to be uploaded to your web server, where the old version of osTicket is running - overwriting the existing files. This can be accomplished by decompressing the download and then using an FTP client to transfer files in *upload directory/folder* to your server, overwriting existing osTicket files. For user using control panels like CPanel or Plesk, you can utilize the systems file manager to upload the package to your server then simply extract the package while making sure the path hierarchy is maintained.

#. Make sure you backup your site's database and files **PLEASE DO NOT SKIP**
#. Upgrader requires user with admin privileges
#. It is recommended that you take the system offline during the upgrade
#. Maintain the directory hierarchy to make sure files are overwritten
#. Upload folder contains the osTicket files that need to be uploaded to your web server.
#. Do not overwrite your ost-config.php file (in the include directory) or else you will lose your MySQL admin settings.
#. Do not upload files in scripts folder. Only useful for remote piping
#. For versions 1.6 RC1-RC2 Only: Once you've overwritten the files, rename config.php to ostconfig.php (config.php is found in root osTicket directory).
#. For newer versions the config.php or ostconfig.php file should be renamed to ost-config.php and moved to the /include folder.


**Note:** If you've customized your osTicket installation, you will need to port the changes to the new version following a successful upgrade. Database changes might cause conflicts.

Running Upgrade Script
----------------------

osTicket ships with web-based upgrade wizard to help guide you through the upgrade process. While the wizard provides step by step guide it is important and helpful to have general knowledge about Web servers, PHP and MySQL. Any errors at this stage, although unexpected, are fatal and might require restoring previous version.

To run the upgrade script, simply login to admin panel of your osTicket helpdesk. The upgrader is now a primary component of the osTicket, so upgrades are triggered automatically anytime you upload a new version which requires a database migration.

When you access the admin panel, the upgrade wizard will be presented and will automatically walk you through the database migration process. Your helpdesk will remain offline, and your staff will be unable to do anything in the staff panel until the database migration has completed.

**Warning:** If you are upgrading from osTicket 1.6 to osTicket 1.7 and above, please ensure that your attachment upload folder has read and write permission for your http server software. Attachments that are not readable by the http server will be lost in the upgrade process.

Post Upgrade Testing
--------------------

Once the upgrade has completed, browse to the staff control panel (scp) and check basics such as viewing and responding to test tickets to ensure things still work as expected. After verifying that the upgrade completed correctly do the following:

#. Enable the help desk
#. Delete setup directory
#. Explore any new feature—see Release Notes
#. Take a minute to send us feedback

**Migration**

We plan on supporting data migration from previous discontinued versions of osTicket as well as 3rd party help desks in the near future. Please check the `forums <https://forum.osticket.com/>`_ for up to date discussions on the subject.
