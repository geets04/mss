.. _content-platform:

Content Platform
================

Web Server
----------
The My sCool Server comes pre-configured with a ready to use web server
to help you host your content and make it available on the local
network.

Hosted content can be accessed from all clients powered by the MSS via any web browser at

::

  http://server/

Hosting custom conent 
^^^^^^^^^^^^^^^^^^^^^

Boot into ``Admin-Desktop``, login as *mssadmin* and put the content to be hosted for all users of the MSS at –

::
 
  /var/www/html/mss/custom

The instructions for customisation of the custom content tile are available via a browser at 

::

  http://server/mss/custom

.. note:: Do ensure that all content to be hosted should have the the following minimum permissions - read and execute for folders and read for files for the target audience.

.. rubric:: Setting correct permissions via Terminal

Execute the following commands in a terminal to ensure requisite permissions -

::
  
  sudo find /var/www/html/mss/custom -type d -exec chmod a+rx {} \;
  sudo find /var/www/html/mss/custom -type f -exec chmod a+r {} \;

Independent content hosting
^^^^^^^^^^^^^^^^^^^^^^^^^^^

There could be a need for each user to host their own HTML based web content. Each user can host her independent content at

::
 
  /home/<username>/public_html 
  
and it may then be accessed by all connected clients at
  
::
  
  http://server/~<username>
  
.. note:: Do ensure that all content to be hosted should have the the following minimum permissions - read and execute for folders and read for files for the target audience.
