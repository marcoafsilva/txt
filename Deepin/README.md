# Configurating Deepin

## Quick Start

### Disableing AppArmor to Docker work properly

```
sudo mkdir -p /etc/default/grub.d

sudo echo 'GRUB_CMDLINE_LINUX_DEFAULT="$GRUB_CMDLINE_LINUX_DEFAULT apparmor=0"' >> /etc/default/grub.d/apparmor.cfg

sudo update-grub

sudo reboot
```
