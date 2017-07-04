i3-cinnamon
===========

This is a package for Arch Linux, to use the i3 window manager within a Cinnamon-session.

Shamelessly stolen from i3-gnome (https://aur.archlinux.org/packages/i3-gnome), licensed under GPLv2.

## Screensaver / i3lock
As of version 0.3, i3-cinnamon will automatically start cinnamon-screensaver. This is done so Cinnamon can automatically lock the screen on special occasions (closing the lid, pressing XF86ScreenSaver, administrative command via loginctl, etc).

If you want to use a different screensaver, say i3lock, edit `i3-cinnamon.session` and remove `cinnamon-screensaver` from `RequiredComponents`.

## Hotkeys
Cinnamon, just like other modern desktops, handles keybindings via its window manager. Thus, with i3-cinnamon every keybinding has to be configured via your i3 config. You can use dbus-send to still make use of cinnamon-settings-daemon(s) though:

### Screen brightness
Increase Brightness:
`dbus-send --dest=org.cinnamon.SettingsDaemon.Power --type=method_call /org/cinnamon/SettingsDaemon/Power org.cinnamon.SettingsDaemon.Power.Screen.StepUp`
Decrease Brightness:
`dbus-send --dest=org.cinnamon.SettingsDaemon.Power --type=method_call /org/cinnamon/SettingsDaemon/Power org.cinnamon.SettingsDaemon.Power.Screen.StepDown`

### Keyboard Backlight
Increase Brightness:
`dbus-send --dest=org.cinnamon.SettingsDaemon.Power --type=method_call /org/cinnamon/SettingsDaemon/Power org.cinnamon.SettingsDaemon.Power.Keyboard.StepUp`
Decrease Brightness:
`dbus-send --dest=org.cinnamon.SettingsDaemon.Power --type=method_call /org/cinnamon/SettingsDaemon/Power org.cinnamon.SettingsDaemon.Power.Keyboard.StepDown`
Toggle On/Off:
`dbus-send --dest=org.cinnamon.SettingsDaemon.Power --type=method_call /org/cinnamon/SettingsDaemon/Power org.cinnamon.SettingsDaemon.Power.Keyboard.Toggle`
