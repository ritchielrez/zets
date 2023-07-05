# How to install nwg-look in Debian 12

[nwg-look](https://github.com/nwg-piotr/nwg-look) is an alternative to **lxappearance**, which supports **Wayland** officially. That means no more messing with gsettings manually, you can change
your GTK, icon and cursor theme reliably globally in *Wayland*. This works the best with *sway window manager*, so specially recommended if you are using it so.

## Installation
Just download the latest tarball from the releases page of **nwg-look's** Github page. Extract it to a folder.
Then copy files from the following folder to the following destinations:
```
nwg-look               -> /usr/local/bin/nwg-look
langs/                 -> /usr/share/nwg-look/langs/
stuff/main.glade       -> /usr/share/nwg-look/main.glade
stuff/nwg-look.desktop -> /usr/share/applications/nwg-look.desktop
```

Run `GTK Settings` from your applications menu, **nwg-look** should launch now, enjoy!!

## Configuration

If you are using *sway*, and you have manually tweaked **gsetttings** stuffs from your config,
then remove them. No longer need to follow this [GTK 3 settings on Wayland](https://github.com/swaywm/sway/wiki/GTK-3-settings-on-Wayland) guide or [this video of mine](https://www.youtube.com/watch?v=1HE6kbpbDS8). Just use **nwg-look** to change your theme an it should just work, hurray!!
