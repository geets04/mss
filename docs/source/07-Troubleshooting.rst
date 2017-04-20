Troubleshooting
===============

Booting or Freezing Problem
---------------------------

If the client machines do not boot or they freeze while working, it can be caused by a faulty network cable, connection or switch. Try connecting a client directly to the server using a LAN cable and attempt booting the client. If the client boots, it confirms that the client and server both are in working order. Then continue troubleshooting your physical network or contact your network engineer.

In case the client machines still do not boot after trying all above steps, :ref:`contact the MSS support team <contact-info>`.

Top Panel Missing
-----------------

If the top panel does not show up execute the following –
::

  Alt+F2 -> resetpanel

Restore Desktop to Default Settings
-----------------------------------

To restore the desktop to default settings of any user run this in terminal from mssadmin account login once the user has logged out –
::

  sudo mv /home/<username>/.config /home/<username>/.config-backup

Next ask the user to login again.

*or*

Users can also try this from a running session -
::

  Alt+F2 -> resetdesktop

User will need to log out and back in for changes to apply.

Remote Desktop Connection Issues
--------------------------------

Try the following steps as mssadmin user (enter password when prompted) -

Check the status of the service
::

  sudo systemctl status xrdp
    
Restart the service
::

  sudo systemctl restart xrdp
    
To check the XRDP processes running
::

  ps ax | grep xrdp
    
Log files related to XRDP
::

  sudo tail -f /var/log/xrdp-sesman.log

To specifically diagnose rdp login issue.
::

  sudo tail -f /var/log/auth.log 
    
Try a user part from one that may currently be logged into an active session.
