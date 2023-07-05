# Scroll speed Xorg

To change the scrolling speed in Xorg, specially in a tiling window manager,
you need xinput, which you can install in Arch Linux, by installing this
package `xorg-xinput`. Then checkout the properties, that are avalaible 
to change for your touchpad:
```bash
xinput list-props device_number_touchpad
```
Run `xinput list` to find out what's your touchpad device number.

After listing all the properties, for me, there's **Scrolling Pixel Distance**
property, which I can change to increase/decrease my scrolling speed. 
A property has a property number besides it in brackets, which can be used to 
change it's value. For **Scrolling Pixel Distance** has a property number of **333**. 
So to change it's value, run:
```bash
xinput set-prop device_number_touchpad property_number property_value
```
