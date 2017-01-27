Backup and Recovery
===================

MSS provides ‘Factory Restore’ option via boot menu or special USB
created with the tool recovery.sh. Factory Restore will restore the
system to the state the server left our premises, which may include
customizations such as user accounts etc if the data is given at the
time of order placement.

-  Multiple snapshots can be created, it is limited by space allocated >
   to /recovery partition, however we are using borg deduplicated >
   backup so only the changes made to system are stored on rerun of >
   the following command as root (sudo su -):

   recovery.sh create

-  To restore to factory from running system, run the following as root
   > (sudo su -):

   recovery.sh restore [optional snapshot number]

-  Snapshots are numerical, 1 being the factory, by default running >
   restore will restore to that snapshot, to restore to last snapshot >
   taken run the following as root (sudo su -):

   recovery.sh restore last

-  To list all snapshots:

   sudo borg list /recovery/system

Snapshot management is beyond the scope of this tool and document, refer
borg documentation for details:
`*http://borgbackup.readthedocs.io/en/stable/usage.htm* <http://borgbackup.readthedocs.io/en/stable/usage.htm>`__

-  To create snapshot of /home for example:

   borg init --encryption=none /backup/folder/path /home

   borg create --stats --progress --compression lz4
   /backup/folder/path/home::snapshotname /home

/backup/folder/path/ must have sufficient space.

-  To restore /home from snapshot

   borg mount /backup/folder/path/home::snapshotname /mnt

   rsync -avP /mnt/\* /home/

When done:

::

    umount /mnt
