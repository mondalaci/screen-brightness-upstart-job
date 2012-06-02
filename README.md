Screen brightness Upstart job
=============================

A lot of Linux users find it disturbing that screen brightness doesn't get saved across reboots.  This is an Upstart job that stores/restores the brightness of the screen upon shutdown/startup.

Installation
------------

Simply copy `screen-brightness.conf` to `/etc/init` as root.  Then reboot.  After that use your computer as usual.  Upon shutting down / rebooting the brightness of your screen will be remembered and restored upon the next boot.