Installation
============

osTicket comes with its own web-based installer to help guide you through the installation process without the frustration. While the installer provides step by step guide during the installation process, it's important and helpful to have general knowledge about Web servers, PHP and MySQL.

Prerequisites
-------------

To install osTicket, your server must have Apache/LiteSpeed/IIS webserver (with the URL Rewrite module installed/enabled), PHP 8.1 - 8.2 (8.2 recommended), and MySQL 5.0 (or better) installed. If you are unsure whether your server meets these requirements, please check with your host or webmaster before proceeding with the installation.

You will need one MySQL database with valid user, password and hostname handy during installation. MySQL user must have FULL privileges on the database. If you are unsure whether you have these details or if the user has sufficient permissions, please consult your host or database admin before proceeding.

**WINDOWS RECOMMENDED LINKS**

#. PHP 8.2 for Windows Server `64-bit <https://windows.php.net/downloads/releases/php-8.2.6-nts-Win32-vs16-x64.zip>`__ | `32-bit <https://windows.php.net/downloads/releases/php-8.2.6-nts-Win32-vs16-x86.zip>`__
#. PHP 8.1 for Windows Server `64-bit <https://windows.php.net/downloads/releases/php-8.1.16-nts-Win32-vs16-x64.zip>`__ | `32-bit <https://windows.php.net/downloads/releases/php-8.1.16-nts-Win32-vs16-x86.zip>`__
#. MySQL 8.0 for Windows Server `64-bit <https://cdn.mysql.com/Downloads/MySQLInstaller/mysql-installer-web-community-8.0.32.0.msi>`__
#. MariaDB 10.11 for Windows Server `64-bit <https://dlm.mariadb.com/2873464/MariaDB/mariadb-10.11.2/winx64-packages/mariadb-10.11.2-winx64.msi>`__
#. PHP Manager 2 for IIS (makes managing PHP on IIS much easier) `here <https://www.phpmanager.xyz/>`_

Getting Started
---------------

At this point you should have downloaded `latest version <https://osticket.com/download>`_ of osTicket. Uncompress the files and upload files and directories in :code:`upload` folder to a directory of your choice on your server. For example :code:`/osticket/`, :code:`/helpdesk/` or :code:`/support/` depending on your preference. Basic knowledge of using FTP is a plus at this stage. If you don't know how to use FTP, we would recommend you read the documentation supplied with your FTP client and learn the basics of uploading and setting permissions on files.

osTicket installer needs to be able to write and modify :code:`ost-config.php` found in the include directory. Please follow the instructions given by the installer.

Using Installation Script
-------------------------

Once all of the above steps are complete, you can complete the installation and basic setup in a web browser. You can invoke the installer by simply browsing the osTicket URL e.g :code:`http://www.yourdomain.com/support`. Alternatively you can enter the URL to it into your browser address bar e.g :code:`http://www.yourdomain.com/support/setup/`.

osTicket's installation script will attempt to auto-detect paths and any permission issues. Please follow the instructions to finish up the installation process.

#. If the script spots any configuration errors then it will not allow you to continue until the errors are corrected.
#. If everything checks out, you will be presented with a form to fill in the required information.
#. If any errors occurs, go back and check the data entered.
#. On valid data the script will create and populate the database plus write a configuration file.

Note that the installer performs basic configuration required to get osTicket up and running. Further configuration is required, post-install, to make the system fully functional.

Installing osTicket Using Fantastico In CPanel
----------------------------------------------

osTicket can also be installed on CPanel based web hosting accounts using Fantastico.From your CPanel, click on Fantastico and follow the instructions to install osTicket.

**IMPORTANT:**

#. The Fantastico default installation package (as of 9 Jan 2010) installs osTicket with the default email address of support@system.com. If you install using Fantastico, you MUST immediately change your default email addresses in the main System Preferences and in your Department settings.
#. The Fantastico package for osTicket may not be as up to date as the latest release available on osTicket.com. Please check the osTicket.com website for the most up to date version.

Finishing Up
------------

If the setup script has finished running with no errors, then congratulations osTicket is now installed. You can now log in with the username and password you created during the install process. After verifying that the installation completed correctly - your next step should be to fully configure your new support ticket system for use. But before you get to it please take a second to cleanup.

#. Change permission of include/ost-config.php to remove write access
#. Delete setup directory
#. Enable the system

Once you have done the above, you can proceed with the next step, Post-Install Setup.

**HAVING TROUBLE**

We can help install and configure osTicket to your needs. Please learn more about our `professional installation services <https://osticket.com/services/professional-support/>`_.

Self-Help Troubleshooting
-------------------------

If you can not find any solutions to the problem you are having, you can enable the "Show Errors" flags located in :code:`/bootstrap.php` (or :code:`/main.inc.php` in older versions):

.. code-block:: bash

   # Don't Display Errors
   ini_set('display_errors',0);
   ini_set('display_startup_errors',0);

Change this to:

.. code-block:: bash

   ini_set('display_errors',1);
   ini_set('display_startup_errors',1);

Then errors should be displayed either in your web browser or in your server's :code:`error.log` file.

Moreover, don't forget to check your osTicket Dashboard page and your mail server log.
