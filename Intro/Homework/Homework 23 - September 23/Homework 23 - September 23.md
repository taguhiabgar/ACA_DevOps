[https://superuser.com/questions/1358080/what-does-grub-default-12-mean/1358087#1358087](https://superuser.com/questions/1358080/what-does-grub-default-12-mean/1358087#1358087)

[https://askubuntu.com/questions/82140/how-can-i-boot-with-an-older-kernel-version](https://askubuntu.com/questions/82140/how-can-i-boot-with-an-older-kernel-version)

```
558  cat /etc/sysctl.conf 
  559  sysctl 
  560  sysctl -a
  561  sysctl -a | grep forward
  562  vim /etc/sysctl.conf 
  563  sysctl -p
  564  sysctl -a | grep forward
  565  exit
  566  sysctl -a | grep max
  567  sysctl -a | grep fs.file-max 
  568  dpkg --list | grep linux-image
  569  cleaar
  570  clear
  571  dpkg --list | grep linux-image
  572  sudo grub-mkconfig | grep -iE "menuentry 'Ubuntu, with Linux" | awk '{print i++ " : "$1, $2, $3, $4, $5, $6, $7}'
  573  uname -srn
  574  vim /etc/default/grub
  575  sudo update-grub
  576  sudo systemctl reboot
  577  uname -srn
  578  sudo grub-mkconfig | grep -iE "menuentry 'Ubuntu, with Linux" | awk '{print i++ " : "$1, $2, $3, $4, $5, $6, $7}'
```
