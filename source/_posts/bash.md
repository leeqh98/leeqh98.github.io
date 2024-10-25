# the art of command line

## Bash command
apt apt-get yum dnf
* bash the linux document project; man bash; zsh fish

* Vim / vi
* man apropos help / help -d type command
* > < | >> ; stdout stderr 
* awk sed head cat tail 
* * ? ... ' " # regex
* & ctrl-z ctrl-c jobs fg bg kill # zhongduan dos
* ssh ssh-agent ssh-add
* ls ls -l less head tail tail -f less +F ln ln -s 
* chown chmod du du -hs * df mount fdisk mkfs lsblk ls -i df -i
* ip ifconfig dig
* git

## binary tools
* objdumps
* readelf
* strings
* grep egrep -i -o -v -A -B -C 

----

glibc libstdc++ : library of c/c++
kernel
document manpages manpages-dev manpages-posix
etc.
faq; reference debian 
## bash mode
.bashrc

set -o vi
$HOME/.inputrc
set editing-mode vi
set keymap vi
set show-mode-in-prompt on # (bash >= 4.3)

set keymap vi-command 
Control-l: clear-screen

set keymap vi-insert
Control-l: clear-screen


