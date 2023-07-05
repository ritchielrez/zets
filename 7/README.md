# Window titles and classes in i3wm

OMG, TerminalForLife is awesome, a great resource to learn stuff
about Linux and i3wm. His [i3wm config](https://github.com/terminalforlife/i3Config) is just lit.
It's a good resource to learn about how to use window titles and
classes effectively to manage different kindoff windows and popups 
for different apps. Like I like my main firefox window to be tilled,
but the popups to be floated, so I can follow this syntax to set up
that:
```
for_window [class="^Firefox$" title="^Mozilla Firefox$"] floating disable
for_window [class="^Firefox$" title="^Close Firefox$"] floating enable
```
Here, I'm explicitly saying that, if a window, has a class name starts with "Firefox",
and the **title = "Mozilla Firefox"**, tile it. Otherwise if the **title = "Close Firefox"**, 
make it a floating window.    

If you're unsure about the window's class and title, you can use `xprop`, then select a window 
to figure it's class and title. Generally the window class is equals to `WM_CLASS` property. 
It's normal for a window to have 2 classes. But in case for a window title, there should be a single value, 
which is equals to the `WM_NAME` property.    

Classes are based on what application the window is from. And
name is the unique identifier between window of the same app. Like all the **Firefox** 
windows have 2 classes, `Firefox` and `firefox`, but only the main window 
is called `Mozilla Firefox`, it's the name of it.   

Now what about implicitly refer to a window class or window title? Well here is how you do it:
```
for_window [class="^Firefox$" title="^Clear All History$"] floating enable
```
This means, enable floating if the window belongs to **Firefox** and also if the 
window title starts with **"Clear All History"**. This same techinic can be used 
for other applications as well. Last trick, if you want to disable titlebars
for all sorts of window, you can do this in your config:
```
for_window [class="^.*"] border pixel 0
```
This makes border of every window to be 0 pixel.
