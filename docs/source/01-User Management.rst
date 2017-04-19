.. _user-management:

User Management
===============
Via GUI:
--------
 
 System → Administration → Users and Groups

Via Commandline:
----------------
Login as mssadmin and then execute the following commands in a terminal –

To switch to root user privileges –
:: 
 sudo su
To add a new user –
::
 useradd -m username
To set a password for a previously created user –
::
 passwd username
To add a user to epoptes group, needed only for teachers and admin accounts –
::
 usermod -a -G epoptes username
By default, the appliance is shipped with the following user accounts pre-configured i.e. if no customisation has been requested during order placement –

**student accounts:** student1 to student100; **password:** 12345

**teacher accounts:** teacher1 to teacher10; **password:** imteacher
