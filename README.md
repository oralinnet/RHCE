# RHCE 8/9
RHCE with ansible 

## Pre-requisits    
-   ssh server configuration 
-   password and keybase authentication 
    -   sshkey-gen
    -   ssh-copy-id
    -   ssh private key ssh public key 
-   sudo configuration 
-   web server configuration 
-   enable / disable service 
-   start / stop service 
-   firewalld    
## Ansible Documentation 
-   [Ansible Document](https://docs.ansible.com/)

## Ansible Install 
```sh
yum install ansible 
```
## RHEL Subscribe

-   Create RHN id / RedHat account in [redhat](https://www.redhat.com/)
    -   Register System with redhat
    -   Attach pool for ansible
    -   Enable repos for ansible
    -    dnf install ansible -y

## Subscribe your system
```sh
subscription-manager register
subscription-manager list --available
subscription-manager attach --pool=<pool id>
subscription-manager repos --enable ansible-VERSION-for-rhel-8-x86_64-rpms
subscription-manager repos --enable ansible-2.9-for-rhel-8-x86_64-rpms
yum install bash-completion
```
## Learning Step 

-   Step 1: [install ansible](https://github.com/oralinnet/RHCE/blob/main/install_ansible/README.md)
-   Step 2: [sudo Privilege](https://github.com/oralinnet/RHCE/blob/main/sudo_privilege/README.md)
-   Step 3: [ssh keybase login](https://github.com/oralinnet/RHCE/blob/main/ssh/README.md)
আমার সোনার বাংলা
