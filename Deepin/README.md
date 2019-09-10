# Configurating Deepin

## Quick Start

### Disableing AppArmor to Docker work properly

```
sudo mkdir -p /etc/default/grub.d

sudo echo 'GRUB_CMDLINE_LINUX_DEFAULT="$GRUB_CMDLINE_LINUX_DEFAULT apparmor=0"' >> /etc/default/grub.d/apparmor.cfg

sudo update-grub

sudo reboot
```

### Create terminal alias

```
sudo vim ~/.bashrc

# -----------
# Aliases ---
# -----------

alias gs='git status'
alias gaa='git add .' 

alias update='sudo apt-get update'
alias upgrade='sudo apt-get upgrade'
alias dist-upgrade='sudo apt-get dist-upgrade'
alias system-upgrade='update && upgrade && dist-upgrade'
```