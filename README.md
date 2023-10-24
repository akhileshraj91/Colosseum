# Colosseum
SMARTCOMP

## LXC launch commands
```bash
lxc image import ./base-1604-cuda.tar.gz --alias my-base-image
lxc launch my-base-image 
```

## LXC ensure networking
```bash
lxc exec container_name -- /etc/init.d/networking restart
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
