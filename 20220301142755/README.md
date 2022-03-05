## Force quit applications in Linux

**Xkill** is the best program to force quit or kill an app, that just crashed.
This is more useful than `pkill` or `killcall` command, as it seems to 
be better at force quitting off crashed applications.

Install `xkill` with this command in Arch Linux `sudo pacman -S xorg-xkill` and 
bind a keymap to run xkill, so you have a quick but effective way to close crashed 
applications, in both Xorg and Wayland.

### PS: In wayland, xkill requires *xwayland* to be installed