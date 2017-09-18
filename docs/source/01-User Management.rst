.. _user-management:

User Management
===============

Create new user 
---------------

Boot into ``Admin-Desktop``, login as *mssadmin* and perform these steps –

**Via GUI**
 
 System → Administration → Users and Groups

Add new user by pressing the ``+Add`` button, once the existing user list has loaded.

Thereafter set the new user's password when prompted.

**Via Terminal**

::

 sudo useradd -m <username>

Enter *mssadmin's* password when prompted and continue.


Adding a user to *epoptes* group (needed only for teacher accounts) –
::
 
 usermod -a -G epoptes <username>


Change password 
---------------

.. _change_own_password:

To change your own password 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Via GUI**
::
 
 Alt+F2 -> ltsp-remoteapps users-admin

Press ``Change...`` against the ``Password:`` label. Thereafter set your password in the ``Change User Password`` dialog.

**Via Terminal**
::
 
 Alt+F2 -> ltsp-remoteapps xterm -> passwd

.. _change_other_password:

To change password of other user
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Boot into ``Admin-Desktop``, login as *mssadmin* and perform these steps -

**Via GUI**
 
 System → Administration → Users and Groups

Select the user whose password needs changing. Press ``Change...`` against the ``Password`` label. Authenticate with *mssadmin's* password when prompted. Finally set new password in the ``Change User Password`` dialog.

**Via Terminal**
::

 sudo passwd <username>

Enter *mssadmin's* password when prompted and continue.
 

Mass user addition
------------------

For adding  several users at one go, boot into ``Admin-Desktop``, login as *mssadmin** and perform these steps -

* Create space separated file containing "username password" such as this :download:`sample </files/users.csv>`. 

   Steps:
   
   * Use LibreOffice Calc to create the file
   * Choose ``File -> Save as``. You will see the ``Save as`` dialog.
   * In the ``File type`` field select the format ``Text CSV (.csv)``.
   * Enter a file name as users.csv and click ``Save``.
   * From the ``Export of text files`` dialog that appears, select the field delimeter as ``{space}`` for the data to be exported, and press OK. 
   
   **Note:** There should be no empty lines in the file. 

* Open terminal and execute the command –

::

 sudo massuseradd <path_to_csv_file>

Example: 
:: 

 sudo massuseradd /home/mssadmin/users.csv

Default credentials
-------------------

By default, the appliance is shipped with the following user accounts pre-configured i.e. if no customisation has been requested during order placement –

==================  ============  ===========
Account Type        Username      Password
==================  ============  ===========
Admin 		    mssadmin	   myskool
Student             student<n>    12345
Teacher		    teacher<n>    imteacher
==================  ============  ===========

**It is strongly recommend that a user must change the account password upon first time use.**
