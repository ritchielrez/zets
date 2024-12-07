# How to install azote in Debian 12

[azote](https://github.com/nwg-piotr/azote) is a GUI wallpaper picker for both **X11** and **Wayland** in ***Linux***. It is part of the [nwg-shell](https://nwg-piotr.github.io/nwg-shell/) project.

## Installation

To install **azote**, first download these dependencies:
```bash
sudo apt install python3 python3-setuptools python3-pillow python3-cairo python3-send2trash python3-gi python3-gi-cairo gir1.2-gtk-4.0
```

Then download the source code from the releases page on [azote](https://github.com/nwg-piotr/azote)'s Github page. Extract the downloaded source code, `cd` into the extracted folder. Run the
following command to install **azote**:
```bash
sudo /usr/bin/python3 setup.py install --root="/" --optimize=1
```

## Configuration

If you are using sway, then in the configuration file of sway, change the line starting with the `output` command with this:
```bash
exec ~/.azotebg
```

For other **X11/Wayland window managers**, check the github page for more info.
