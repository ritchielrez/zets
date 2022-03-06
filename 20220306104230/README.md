## Pacman is in use error

**Pacman is in use error** is an common error in Arch Linux. 
This happened when you force quit from an `pacman` proccess.
Like pressing `Ctrl-C` when `pacman` is used for installing 
any program or updating your system.

To fix this error, remove `pacman` database lock:
```bash
sudo rm /var/lib/pacman/db.lck
```
