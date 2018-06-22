Backup and Recovery
===================
We understand that accidents happen and that everyone deserves a second chance. Being open-source one may be tempted to play around with the server and we do not penalise you for doing so. The My sCool Server provides ``Factory Restore`` options via –

1. Server boot menu or
2. USB created with the recovery.sh tool

Factory Restore option restores the system to the state the server left Recherche’s premises, which may include customisation such as user accounts etc., if the data is given at the time of order placement.

.. warning:: Exercise caution before using the ``Factory Restore`` feature. It shall override any customisations done by the user to the server and shall restore it to the factory shipping state. It may also delete user created data. Hence, if user generated data is of value, it is strongly recommended that ``/home`` data is periodically backed up on an external media by following the steps below.

.. note:: The ``Factory Restore`` feature does not restore any preloaded or custom loaded web-content. Backup and restoration of all content accessible via ``http://server`` is the responsibility of the end-user. Read below for easy and useful backup steps. 

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

   borg init --encryption=none </backup/folder/path/home>

   borg create --stats --progress --compression lz4 </backup/folder/path/home>::<snapshotname> /home

/backup/folder/path/ must have sufficient space.

-  To restore ``/home`` from snapshot:

::

   borg mount </backup/folder/path/home>::<snapshotname> /mnt

   rsync -avP /mnt/* /home/

When restoration is complete:

::

    umount /mnt

Pre-loaded Content Locations
^^^^^^^^^^^^^^^^^^^^^^^^^^^
Most of the preloaded web content resides at the common location - ``/var/www/html/mss``. However some of the content that have their own custom location are listed below - 

:NROER:
 /home/docker
:Gyankunj Slate:
 /home/mssadmin/slate
:ePathshala:
 /home/mssadmin/.epathshala
