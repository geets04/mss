Troubleshooting
===============

Booting
-------

If the client does not boot or freezes while working - It can be caused
by faulty network cable, connection or switch, try direct connection to
the server to ensure that the client and server both are in working
order then troubleshoot physical network.

Panel
-----

If the panel does not show up -

Alt+F2 -> resetpanel

Default settings
----------------

To bring the desktop to default settings of any user run this in
terminal from mssadmin account login -

::

    sudo mv /home/username/.config /home/username/.config-backup

Users can also try this from running session -

Alt+F2 -> resetdesktop

Will need log out and back in for changes to apply.

XRDP Remote Desktop Connection
------------------------------

Check the status of the service
    systemctl status xrdp
Restart the service
    systemctl restart xrdp
To check the XRDP processes running
    ps ax | grep xrdp
log files related to XRDP
    tail -f /var/log/xrdp-sesman.log
    tail -f /var/log/auth.log # for login issue 
Try different users, the one not already logged in
