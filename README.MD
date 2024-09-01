# Rainbow Dash Boot Animation
This is a plymouth theme featuring animation of rainbow dash flying. **This package is only for debian-based operating system**. Popular debian-based OS include but not limited to Debian, Ubuntu, Kali Linux, and Linux Mint. **Other operating system like Windows, iPhone and Android can't install this**.

## Download
Open release section to [download](https://github.com/yeaayy/plymouth-theme-rainbow-dash/releases/latest).

## Building
Just run
```sh
./build
```
from project root directory and it should output the package to `plymouth-theme-rainbow-dash_<version>_all.deb`. Where `<version>` is version of the theme (currently it).

## Installing
After download or build the package run
```sh
sudo dpkg -i plymouth-theme-rainbow-dash_<version>_all.deb
```

## Removing
```sh
sudo dpkg -r plymouth-theme-rainbow-dash
```

## Temporary Removal
### Temporary Removal on Kali Linux
To temporarily switch back to default Kali Linux boot animation run
```sh
sudo plymouth-set-default-theme kali -R
```
---
To switch back again to this boot animation run
```sh
plymouth-set-default-theme rainbow-dash -R
```

### Temporary Removal on Linux Mint
```sh
sudo update-alternatives --config default.plymouth
```
choose  `/usr/share/plymouth/themes/mint-logo/mint-logo.plymouth`, then run:
```sh
sudo update-initramfs -c -k $(uname -r)
```
---
To switch back again to this boot animation run:
```sh
sudo update-alternatives --config default.plymouth
```
choose  `/usr/share/plymouth/themes/rainbow-dash/rainbow-dash.plymouth` or choose 0, then run
```sh
sudo update-initramfs -c -k $(uname -r)
```

## Test
This package is tested on:
 - Linux Mint
 - Kali Linux (VM)

I haven't try on other distro so if you try to install this package in other distro that aren't mentioned above please let me know, I will update the list and possibly fix it if it doesn't work.
