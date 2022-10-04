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
sudo dnf install -y epel-release 
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
  google-chrome\
  neovim\
  flameshot\
  

sudo snap install firefox thunderbird libreoffice 
```


### todo

- wlr-randr
- sway
