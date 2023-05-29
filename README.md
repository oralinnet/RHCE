# RHCE 8
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
yum install ansible 

## RHEL Subscribe

-   Create RHN id / RedHat account in http://www.redhat.com/                                                            
    -   Register System with redhat
    -   Attach pool for ansible
    -   Enable repos for ansible
    -    dnf install ansible -y

## subscription-manager register
```sh
   subscription-manager list --available
   subscription-manager attach --pool=<pool id>
   subscription-manager repos --enable ansible-VERSION-for-rhel-8-x86_64-rpms                                                  
   subscription-manager repos --enable ansible-2.9-for-rhel-8-x86_64-rpms                                                      
   dnf -y install ansible
   yum install bash-completion
```