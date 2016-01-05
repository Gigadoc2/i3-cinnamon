i3-cinnamon
===========

This is a package for Arch Linux, to use the i3 window manager within a Cinnamon-session.

Shamelessly stolen from i3-gnome (https://aur.archlinux.org/packages/i3-gnome), licensed under GPLv2.

## Screensaver / i3lock
As of version 0.3, i3-cinnamon will automatically start cinnamon-screensaver. This is done so Cinnamon can automatically lock the screen on special occasions (closing the lid, pressing XF86ScreenSaver, administrative command via loginctl, etc).

If you want to use a different screensaver, say i3lock, edit `i3-cinnamon.session` and remove `cinnamon-screensaver` from `RequiredComponents`.
