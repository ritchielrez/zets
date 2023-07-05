# How to install eww in Debian 12

[eww](https://elkowar.github.io/eww/) is the **Rainmeter** of **Linux**. It can be used to create various widgets in the lsp language. Even though 
this program has been developed for a while, it is still recommended to compile it from source
using cargo and rustc nightly toolchain. Repository packages are not recommended to use.

First you need to download [rustup](https://rustup.rs/). Go to the website and run the following
command listed on the website. Make sure to customize the installation to install nightly toolchain, keep the other options to default.

Then install dependecies with the package manager:
```bash
sudo apt install libqt5glib-2.0-0 libspice-client-glib-2.0-8 libspice-client-glib-2.0-dev libgdk-pixbuf-2.0-dev libgdk-pixbuf2.0-dev librust-atk-dev librust-atk-sys-dev libcairo-gobject2 libcairo-gobject-perl librust-cairo-rs-dev librust-cairo-sys-rs-dev librust-pangocairo-dev librust-pangocairo-sys-dev librust-gdk-pixbuf-dev librust-gdk-pixbuf-sys-dev librust-gdk-sys-dev libgtk-layer-shell-dev -y
```
 After that, follow the [eww](https://elkowar.github.io/eww/) instructions to compile it.
