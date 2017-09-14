.. _user-management:

User Management
===============

To create new user 
-----------------------

Boot with "Admin-Desktop" then perform the following steps –

**Via GUI:**
 
 System → Administration → Users and Groups

**Via Commandline:**

Login as mssadmin and then execute the following commands in a terminal –

To switch to root user privileges –
::
 
 sudo su

To add a new user –
::

 useradd -m username

To set a new password 
-----------------------

To set a password for a previously created user –

**Via GUI :**
::
 
 Alt+F2 -> ltsp-remoteapps users-admin

**Via Terminal :**
::
 
 Alt+F2 -> ltsp-remoteapps xterm -> passwd

To add a user to epoptes group, needed only for teachers and admin accounts –
::
 
 usermod -a -G epoptes username

By default, the appliance is shipped with the following user accounts pre-configured i.e. if no customisation has been requested during order placement –

**student accounts:** student1 to student100; **password:** 12345

**teacher accounts:** teacher1 to teacher10; **password:** imteacher

Mass User Addition:
-------------------

For adding more than one users at a time , create users list in LibreOffice Calc .

Create space separated by "username password" file users.csv (`see sample <https://docs.google.com/spreadsheets/d/1Z7EyS8XjG1j0OxHe8-w_S8ysnXUDn97Ux1-ib4gGoeQ/edit?usp=sharing>`_), there should be no empty lines in the file. 

	Tip : 

	* Use LibreOffice Calc to create the file

	* Choose File -> Save as. You will see the Save as dialog.

	* In the File type field select the format "Text CSV (.csv)".

	* Enter a file name as users.csv and click Save.

	* From the Export of text files dialog that appears, select the field delimeter as {space} for the data to be exported, and confirm with OK.


Open terminal and execute the command –
::

 sudo massuseradd /path/to/file/users.csv
