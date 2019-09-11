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

### Create terminal alias

```
sudo vim ~/.bashrc

# -----------
# Aliases ---
# -----------

# Git -------
alias gs='git status'
alias gaa='git add .' 

# System ----
alias update='sudo apt-get update'
alias upgrade='sudo apt-get upgrade'
alias dist-upgrade='sudo apt-get dist-upgrade'
alias system-upgrade='update && upgrade && dist-upgrade'
```

### Customizing Git 

```
sudo vim ~/.bashrc

PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]$(__git_ps1 " \[\e[1;30;42m\](%s)")\[\e[m\] $ '
```