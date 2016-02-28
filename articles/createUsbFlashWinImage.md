# How to create usb stick with windows on board? #

OK, after unsuccessfully trying all methods mentioned here, I finally got it working. Basically, the missing step was to write a proper boot sector to the USB stick, which can be done from Linux with ms-sys or lilo -M. This works with the Windows 7 retail version.

## Here is the complete rundown again:

Install 'ms-sys' - if it is not in your repositories, get it here. Or alternatively, make sure lilo is installed (but do not run the liloconfig step on your local box if e.g. Grub is installed there!)

Check what device your USB media is assigned - here we will assume it is /dev/sdb. Delete all partitions, create a new one taking up all the space, set type to NTFS (7), and remember to set it bootable:

'cfdisk /dev/sdb   or   fdisk /dev/sdb (partition type 7, and bootable flag)'

Create an NTFS filesystem:

'mkfs.ntfs -f /dev/sdb1'

Write Windows 7 MBR on the USB stick (also works for windows 8), multiple options here:

'ms-sys -7 /dev/sdb'
or (e.g. on newer Ubuntu installs) sudo lilo -M  /dev/sdb mbr (info)
or (if syslinux is installed) sudo dd if=/usr/lib/syslinux/bios/mbr.bin of=/dev/sdb
Mount ISO and USB media:

' mount -o loop win7.iso /mnt/iso'
'mount /dev/sdb1 /mnt/usb'
Copy over all files:

' cp -r /mnt/iso/* /mnt/usb/ '  ...or use the standard GUI file-browser of your system

Call sync to make sure all files are written.

...and you're done.

After all that, you probably want to back up your USB media for further installations and get rid of the ISO file... Just use dd: # dd if=/dev/sdb of=/win7.img

and reverse if/of next time you want to put the Windows 7 installer onto USB.

As always, double check the device names very carefully when working with dd.
