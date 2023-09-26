# linux_command
### centos network config
```
  vi /etc/sysconfig/network-scripts/ifcfg-eth0
```

```
  ifdown eth0 && ifup eth0
```
### Enable UDP on SSH
```
  apt update -y && apt upgrade -y
```  
```
  apt install screen
``` 
```
  apt install lsof
```
```
  wget -O /usr/bin/badvpn-udpgw https://raw.githubusercontent.com/daybreakersx/premscript/master/badvpn-udpgw64
```
```
  chmod +x /usr/bin/badvpn-udpgw
```
```
  nano /etc/rc.local
```
paste this command on /etc/rc.local
```
  #!/bin/sh -e
  screen -AmdS badvpn badvpn-udpgw --listen-addr 127.0.0.1:7555
  exit 0
```
```
  chmod +x /etc/rc.local
```
```
  reboot
```
### Change owner directory on Ubuntu
```
sudo chown -R username:group directory
```

