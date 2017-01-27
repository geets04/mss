Network
=======

MSS comes with 2 predefined network configurations: Static and Dynamic.

If there is no other DHCP server in the network select Static connection
from the NetworkManager in mssadmin account. If there is existing DHCP
server then selecting Dynamic setup will cause MSS to run in proxy-DHCP
mode, IPs will be assigned by external DHCP. Edit the setup which will
not be used to disable ‘auto connect’. No other configuration changes
are required.

.. figure:: images/image00.jpg
   :alt: 

.. figure:: images/image02.jpg
   :alt: 

