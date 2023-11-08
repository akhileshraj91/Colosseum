# Colosseum
SMARTCOMP

## LXC launch commands
```bash
lxc image import ./base-1604-cuda.tar.gz --alias my-base-image
lxc init local:my-base-image my-custom-container
lxc list
lxc image list
lxc start my-base-image
lxc launch my-base-image 
```

## LXC ensure networking
```bash
lxc exec container_name -- /etc/init.d/networking restart
lxc exec container_name /bin/bash
cat /etc/resolv.conf
nameserver 8.8.8.8
nameserver 8.8.4.4
```

## Update Nix
```bash
apt update
apt upgrade
nix-env -iA nixpkgs.git
```
## LXC export and publish 
```bash
lxc stop image
lxc publish image --alias new-name
lxc image export new-name PATH
```
