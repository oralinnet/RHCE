# Enable Sudo Privilege for normal user 

-   A user that has full sudo privileges can run all Linux commands as root.

```sh
visudo
vim /etc/sudoers
# UserList    Machine/system=user     Commands  --- syntax
raju    ALL=(ALL)   /usr/sbin/useradd           ## raju user sudo privilege only useradd command
raju    ALL=(ALL)   NOPASSWD:/usr/sbin/useradd  ## raju user do sudo command without password
ansible     ALL=(ALL)   NOPASSWD:ALL            ## ansible user can execute all root user command 
```
-   save sudoers file 

### sudo privilege for group 

```sh
visudo
vim /etc/sudoers
# UserList    Machine/system=user     Commands  --- syntax
%wheel      ALL=(ALL)   ALL     ## wheel group all user can execute sudo command
%wheel      ALL=(ALL)   NOPASSWD:ALL
gpasswd -a ansible wheel        ## assign ansible to wheel group 
```

### sudo privilege in file 

-   sudoers is sensitive files so you always create a new file for save purpose

```
visudo 
includedir /etc/sudoers.d       ## uncommand this line 
:x
cd /etc/sudoers.d/
vim ansible
ansible     ALL=(ALL)   NOPASSWD:ALL        ## ansible user can sudo command with out password 
```

