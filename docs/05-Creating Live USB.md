Li-f-e: Linux for Education OS image is included on the server and can
be used to create a bootable media when logged in as mssadmin account
via -

System Tools -&gt; Live USB GUI

When creating a bootable media intended to boot computers that only
support EFI booting select “isohybrid” option. This option can also boot
on legacy hardware so use this if you are not sure about your hardware
capabilities. Use of “isohybrid” option is officially recommended way of
creating bootable USB. Do note that this will wipe the USB device and
cannot be used as a normal storage media from Windows PC. Use “Ubuntu”
option if you wish to use the device as a storage media on Windows or
preserve data on a vfat formatted USB stick.

The iso image is located at /recovery/Li-f-e.iso or /home/mssadmin/

It is convenient to use command line for running this task multiple
times as below:

    sudo live-grub-stick --isohybrid /recovery/Li-f-e.iso /dev/sdb

See the following links to learn how to boot from USB stick and
troubleshooting if the USB does not boot:

[*https://www.lifewire.com/change-the-boot-order-in-bios-2624528*](https://www.lifewire.com/change-the-boot-order-in-bios-2624528)

[*https://www.lifewire.com/how-to-boot-from-a-usb-device-2626091*](https://www.lifewire.com/how-to-boot-from-a-usb-device-2626091)
