## Restart KDE Plasma (*terminal* method)

To restart **KDE Plasma** from the terminal, run this command:

```bash
# For KDE 4
killall plasma-desktop && kstart plasma-desktop

# For KDE 5 < 5.10
killall plasmashell && kstart plasma-desktop

# For KDE > 5.10
kquitapp5 plasmashell || killall plasmashell && kstart5 plasmashell
```
