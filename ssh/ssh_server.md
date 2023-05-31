# SSH Server configuration 

-   package: openssh-server 
-   service: sshd
-   port : 22
-   conf file : /etc/ssh/sshd_config

### Install SSH Server 

```sh
yum install openssh-server 
systemctl start sshd 
systemctl enable sshd 
systemctl restart sshd 
```

 ### SSH Server Port Change 

```sh
# change default port 22 to other port then save file
vim /etc/ssh/sshd_config
# Add port to firewall and selinux 
firewall-cmd --permanent --add-port=225/tcp
firewall-cmd --reload
# restart ssh server 
systemctl restart sshd 
```

### root login disabled

```sh
#PermitRootLogin yes change to PermitRootLogin no and remove # 
vim /etc/ssh/sshd_config
# restart ssh server 
systemctl restart sshd 
```


