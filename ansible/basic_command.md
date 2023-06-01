-   Ansible version check 
```sh
ansible --version
```
-   Ansible module check 
```sh
ansible-doc -l
ansible-doc -l | wc -l          ## module cound
ansible-doc yum                 ## ansible yum module info
```
-   Document and rpm location

```sh
rpm -q ansible
rpmquery ansible -c
rpm -qc ansible
```

-   Basic command host and group  
-   Host file default location /etc/ansible/hosts. its declar on ansible cfg file
-   You can only add hostname name here, so use dns server or /etc/hosts file

-   Add remote host in ansible 

```sh
vim /etc/ansible/hosts
## single server

servera
serverb
serverc
serverd

## server group

[web]
servera
serverb

[api]
serverc

[db]
serverc

```

-   Qury from host file 

```sh
ansible all --list-hosts            ## ansible inventory hosts list 
ansible '*' --list-hosts            ## ansible inventory hosts list
ansible 'servera' --list-host       ## check servera host 
ansible server[a-c] --list-hosts    ## check server a-c hosts
ansible ungrouped --list-hosts      ## check ungroup hosts 
ansible web --list-hosts            ## check web group hosts 
```
