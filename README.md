i3-cinnamon
===========

This is a package for Arch Linux, to use the i3 window manager within a Cinnamon-session.

Shamelessly stolen from i3-gnome (https://aur.archlinux.org/packages/i3-gnome), licensed under GPLv2.

## Screensaver / i3lock
In theory, you can use any Screensaver/Screenlocker you want with i3-cinnamon; but Cinnamon will, if installed and running, invoke cinnamon-screensaver to activate on several occasions (closing the lid, pressing a lockscreen-button, getting a lock signal from systemd-logind or similar…).

To prevent this, deactivate the cinnamon-screensaver autostart, by editing cinnamon-screensaver.desktop in your autostart folder.

However, i3lock will NOT be automatically launched by Cinnamon. For this, you would need a wrapper around i3lock, listening on cinnamon-screensavers dbus-interface.
