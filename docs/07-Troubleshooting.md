##Booting
If the client does not boot or freezes while working - It
can be caused by faulty network cable, connection or switch, try direct
connection to the server to ensure that the client and server both are
in working order then troubleshoot physical network.

##Panel
If the panel does not show up -

Alt+F2 -&gt; resetpanel

##Default settings
To bring the desktop to default settings of any
user run this in terminal from mssadmin account login -

    sudo mv /home/username/.config /home/username/.config-backup

Users can also try this from running session -

Alt+F2 -&gt; resetdesktop

Will need log out and back in for changes to apply.