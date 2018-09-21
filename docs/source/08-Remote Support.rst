.. _remote-support:

Remote Support
==============

For getting support remotely from support team, perform the following steps - 

* Login with any account, navigate to ``Applications`` → ``Internet`` →  ``Remmina``

* Do following steps -

 #. ``RDP`` must be selected in dropdown box. 
 #. Type ``server`` as shown below.
 #. Hit ``Connect !``.

 .. figure:: images/remmina.jpg
   :alt: Remote Support - Reminna

* When connection is established, Login as *mssadmin* in remmina screen .

 .. note:: Following steps should be perform in opened remmina window

* Connect Wi-Fi/Hotspot for Internet Connection, see :ref:`connect-wifi` section for getting connected to Internet via Wi-Fi/Hotspot.

* Launch ``Epoptes`` from ``Applications`` → ``Internet`` →  ``Epoptes``

* Select ``Remote support`` option from ``Help`` → ``Remote support``

 .. figure:: images/epoptes.jpg
   :alt: Remote Support - Epoptes

* In ``remote-assistance`` dialog follow the steps below -

 #. In ``Method`` check if ``Graphic(VNC)`` is selected.
 #. In ``Host`` type ``support.myscoolserver.com:5500`` 
 #. Hit ``Connect``.

 .. figure:: images/remote-assistance.jpg
   :alt: Remote Support - Remote Assistance

* On successful connection, ``Status`` will change to ``Connected``. 

.. _connect-wifi:

Connect Wi-Fi/Hotspot
---------------------

For connecting Wi-Fi/Hotspot in MSS, login as *mssadmin* and perform these steps -

* Click on |internet|  from top-right corner of the screen, and click the name of the network you want to connect to.

 .. |internet| image:: images/internet-icon.png

 .. figure:: images/wifi-list.jpg
   :alt: Connect Wi-fi - Wi-fi List

 .. note:: If the name of the network is not in the list, select ``More networks`` to see if the network is further down the list. If you still do not see the network, your device may be out of range or the network might be hidden.


* Type password of *mssadmin* in ``Authenticate`` dialog as shown below and hit ``Authenticate``. 

 .. figure:: images/system-authenticate.png
   :alt: Connect Wi-fi - System Authentication

* It will again prompt for the password with the ``Authenticate`` dialog, type password of *mssadmin* and hit ``Authenticate`` 

 .. figure:: images/system-authenticate-2.png
   :alt: Connect Wi-fi - System Authentication

* If the network is protected by a password, enter the password in ``Wi-Fi Network Authentication Required`` dialog when prompted and click ``Connect``.

 .. figure:: images/wifi-authenticate.png
   :alt: Connect Wi-fi - Wi-fi Authentication

* The network icon will change to |wifi|

 .. |wifi| image:: images/wifi-icon.png

 .. note:: If the connection is not successful, you may be asked for your password again or it might just tell you that the connection has been disconnected. 
