Screen brightness Upstart job
=============================

A lot of Linux users find it disturbing that screen brightness doesn't get saved across reboots.  This is an Upstart job that stores/restores the brightness of the screen upon shutdown/startup.

Installation
------------

Simply copy `screen-brightness.conf` to `/etc/init` as root.  Then reboot.  After that use your computer as usual.  Upon shutting down / rebooting the brightness of your screen will be remembered and restored upon the next boot.

Known issues
------------
I wish there was a way to restore screen brightness earlier in the boot process, but the filesystem has to be mounted for the saved brigthness value to be read.  This is disturbing in some cases.  For example when full disk encryption is used the password gets typed early on when initrd is in charge an Upstart hasn't even started yet.