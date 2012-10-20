Screen brightness Upstart job
=============================

A [lot of Linux users](https://bugs.launchpad.net/ubuntu/+source/gnome-power-manager/+bug/35223) find it disturbing that screen brightness doesn't get saved across reboots.  It is usually either too dark or too bright by default.  This is an Upstart job that stores/restores the brightness of the screen upon shutdown/startup.

Installation
------------

Simply copy `screen-brightness.conf` to `/etc/init` as root.  Then reboot.  From this point on the brightness of your screen will be remembered across reboots.

Known issues
------------
I wish there was a way to restore screen brightness earlier in the boot process, but the filesystem has to be mounted for the saved brightness value to be read.  This is disturbing in some cases.  For example when full disk encryption is used the password gets typed early on at which point initrd is in charge an Upstart hasn't even started yet.