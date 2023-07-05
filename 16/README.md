# How to uninstall compiled version of neovim

Solution from this github issue: https://github.com/neovim/neovim/issues/1415

Run these commands to delete directories where neovim have put it's stuffs:
```bash
sudo rm /usr/local/bin/nvim
sudo rm -r /usr/local/share/nvim/
```
