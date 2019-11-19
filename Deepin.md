# Configurating Deepin

## Quick Start

### Disableing AppArmor to Docker work properly

```
sudo mkdir -p /etc/default/grub.d &&
cd ~ &&
echo 'GRUB_CMDLINE_LINUX_DEFAULT="$GRUB_CMDLINE_LINUX_DEFAULT apparmor=0"' > apparmor.cfg &&
sudo mv apparmor.cfg /etc/default/grub.d/ &&
sudo update-grub &&
sudo reboot 
```
