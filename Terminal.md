# Customizing Linux Terminal

## Quick Start

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

###### Showing short path name

```
sudo vim ~/.bashrc

PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u\[\033[00m\]:\[\033[01;34m\]\W\[\033[00m\]$(__git_ps1 " \[\e[1;30;42m\](%s)")\[\e[m\] $ '


PS1='${debian_chroot:+($debian_chroot)}\u:\W\$ '
```

###### Showing Styled in a new row

```
PS1='\[\033[01;32m\]┌─\u\[\033[01;34m\] @ \w\[\033[0;32m\]$(__git_ps1)\n\[\033[01;32m\]└─\[\033[01;32m\] \$\[\033[0m\033[0;32m\] \[\033[00m\]'
```