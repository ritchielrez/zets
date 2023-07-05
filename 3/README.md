# Cursor themes on Linux

Installing and then setting a cursor theme might be tricky in a Tiling 
Windows Manager. Normally, after download the zip file of your cursor
theme. You have to extract it, then copy the extracted folder to 
***/usr/share/icons/***, which is usually also where your icon themes 
exist.

Then you can set the cursor theme from **lxappearance**, an application
which allows to change themes in any desktop enviroment and WM's. Also,
you can set your cursor theme in `~/.Xresources`, where you wanna put 
this:
```
Xcursor.theme: cursor-theme
Xcursor.size: 16
```
Then run `xrdb ~/.Xresources`, this requires you to have `xorg-xrdb`
package in Arch Linux. This is also needed even you're using a wayland
compositor. Apps like **Spotify** otherwise use the default Adwaita cursor theme.

Some applications like **Firefox**, still might not use your preferred
cursor theme in swaywm, so put this line in my config:
`seat seat0 xcursor_theme 'cursor_theme_name' cursor_theme_size`
  
You can also change your cursor theme with the GNOME configuration tool,
which you may need to use in swaywm, as setting themes for GTK3 applications
don't work on swaywm. So you can say swaywm to run this command at startup:
```bash
gsettings set org.gnome.desktop.interface cursor-theme 'cursor_theme_name'
gsettings set org.gnome.desktop.interface cursor-size 'cursor_theme_size'
```
I usually do this in my sway config:
```
set $gnome-scheme org.gnome.desktop.interface
exec_always {
  gsettings set $gnome-scheme cursor-theme 'cursor_theme_name'
  gsettings set $gnome-scheme cursor-size 'cursor_theme_size'
}
```
Usually, you don't need to do any further config changes to set up your
new favourite cursor theme, but you can change your GTK3 configuration file,
located in `~/.config/gtk-3.0/settings.ini`, then change your cursor theme
but also size from there, changing these 2 lines under `[Settings]` :
```
gtk-cursor-theme-name=cursor_theme_name
gtk-cursor-theme-size=cursor_theme_size
```
