# CentOS Stream 8 installation and re-installation

## Install from boot drive

Choose `Workstation` and `Developpement Tools`
User `is admin` and `doesn't require login`

## Basic conf
In /etc/sysconfig/network-scripts/ifcfg-\*
```
DNS1=1.1.1.1
DNS2=1.0.0.1
```

```sh
sudo systemctl restart network
```

## Installing packages

### Repositories
```sh
sudo dnf install -y https://pkgs.dyn.su/el8/base/x86_64/raven-release-1.0-3.el8.noarch.rpm
sudo dnf install -y epel-release
sudo dnf config-manager --set-enabled powertools
sudo dnf upgrade -y
```

### Snap
```sh
sudo dnf install -y snapd
sudo systemctl enable --now snapd
```

### Packages
```sh
sudo dnf install -y\
  clang\
  llvm\
  git\
  zsh\
  kitty\
  flameshot\
  thunderbird\
  i3\
  i3status\
  i3lock\
  dmenu\
  htop\
  pavucontrol\
  keepassxc\
  openconnect\
  clang-tools-extra


sudo snap install firefox thunderbird libreoffice
sudo ln -s /var/lib/snapd/snap /snap
sudo snap install --edge nvim --classic
```

### Bat
```sh
wget https://github.com/sharkdp/bat/releases/download/v0.22.1/bat-v0.22.1-x86_64-unknown-linux-musl.tar.gz
TODO
```


### todo

- ly
- nvidia
- google-chrome
- feh
- bat
