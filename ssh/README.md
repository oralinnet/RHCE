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

### key base Authentication enable

-   need 1 pair key you can generat it from any system 
-   public key save on remote machine and private key save to your self.

#### where you save public key 
-   in sshd config file 47 line AuthorizedKeysFile      .ssh/authorized_keys
-   location of ssh public key.

#### which user can login 
-   if you put public key on user1 .ssh/authorized_keys location.
        -   here .ssh is directory and authorized_keys is file name 
            then only you can ssh to user1, if you want useing same private key all user can login remote server then in ssh conf file change .ssh/authorized_keys location all user must read permission that location

### command 

```sh
ssh-keygen     # create ssh private and pub key 
ssh-copy-id    # copy ssh key to remote machine
ssh -i locatio/keyname root@ip -p xxx  # connect ssh with key if key name is not authorized_keys with deffrient port

```

### Permission 

-   pub key permission is rw- --- ---
-   private key permission is rw- --- ---
