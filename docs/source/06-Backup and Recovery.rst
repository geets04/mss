Backup and Recovery
===================
We understand that accidents happen and that everyone deserves a second chance. Being open-source one may be tempted to play around with the server and we do not penalise you for doing so. The My sCool Server provides ‘Factory Restore’ options via –

1. Server boot menu or
2. USB created with the recovery.sh tool

Factory Restore option restores the system to the state the server left Recherche’s premises, which may include customisation such as user accounts etc., if the data is given at the time of order placement.

Multiple snapshots can be created. It is limited by space available on the /recovery partition. MSS uses borg deduplicated backup so only the changes made to system since the last backup are stored on subsequent backup attempts.

-  To create a backup, run the following command as root (sudo su -):  
   
::

   recovery.sh create

-  To restore to factory image from a running system, run the following as root (sudo su -):

::

   recovery.sh restore [optional snapshot number]

-  Snapshots are numerical, 1 denoting the factory image. By default, running restore will restore to that snapshot. To restore to last snapshot taken run the following as root (sudo su -):

::

   recovery.sh restore last

Snapshot management is beyond the scope of this tool and document. Refer `borg documentation <http://borgbackup.readthedocs.io/en/stable/usage.htm>`_ for details. 

Herein are just a few examples of what can be done with ``borg``:

-  To list all snapshots:

::

   sudo borg list /recovery/system


-  To create a custom snapshot, for example, creating a snapshot of ``/home``:

::

   borg init --encryption=none </backup/folder/path> /home

   borg create --stats --progress --compression lz4 </backup/folder/path>/home::<snapshotname> /home

/backup/folder/path/ must have sufficient space.

-  To restore ``/home`` from snapshot:

::

   borg mount </backup/folder/path/home>::<snapshotname> /mnt

   rsync -avP /mnt/* /home/

When restoration is complete:

::

    umount /mnt
