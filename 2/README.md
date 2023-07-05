# Pacman script

There is no need for me anymore to use **paru** to download Arch Linux 
packages. Because [Chaotic AUR](../../zets/20220301063411/README.md) can integrate 
with **pacman**. The problem is it's disturbing to run *sudo pacman* all 
the time. Extra characters to type, and more impotantly, I'M LAZY. 

So I made a script, that runs **pacman** with **sudo**. Yes I could have 
just made a alias for that. But aliases often depend on what shell
you're using. So I made simple script, which I put it in ***/usr/local/bin***.
Which is in my **PATH**. Here is it:
```bash
#!/bin/sh
sudo pacman $@
```

Here, **$@** refers to the array of command line arguments which are 
provided to the script. Like here, **-S** and **neovim** is provided
to the script **pac**, as arguments.
```bash
pac -S neovim
```
