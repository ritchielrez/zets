# How to remove snapd completely from Ubuntu

First, remove existing snap packages:
```bash
snap remove firefox
snap remove gtk-common-themes
snap remove gnome-3-38-2004
snap remove snapd-desktop-integration
snap remove snap-store
snap remove core20
snap remove bare
snap remove snapd
```

Run `snap list` to see what snap packages are actually installed. Then remove snap package directories:
```bash
rm -rf ~/snap/
```

Run this command below to prevent snap from reinstalling again, thanks **Linux Mint** team for providing this `apt` configuration:
```bash
sudo cat <<EOF | sudo tee /etc/apt/preferences.d/nosnap.pref
Package: snapd
Pin: release a=*
Pin-Priority: -10
EOF
```

Then remove left over directories:
```bash
rm -rf ~/snap/
sudo rm -rf /snap
sudo rm -rf /var/snap
sudo rm -rf /var/lib/snapd
```

Now, even if you try to install packages like `firefox` or `chromium-browser`, Ubuntu will not be able to install `snapd` as a dependency.
