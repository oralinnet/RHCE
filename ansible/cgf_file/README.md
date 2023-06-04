-   CFG file is a generic preference file that stores settings and configuration information.
-   ansible 2.10 or above cfg file is empty
-   Here I attachd default ansible cfg file
-   So you can follow this file and know the default setting of ansible 

### Ansible cfg file location configuration 

-   Ansible cfg file can configure four way 
-   Four priority list of cfg file 

-   First priority is env file 

```sh
export ANSIBLE_CONFIG=/opt/ansible.cfg          # export cfg file temporary
vim /home/raju/.bash_profile                    # export cfg permanent 
export ANSIBLE_CONFIG=/opt/ansible.cfg
touch   /opt/ansible.cfg                        # must be create cfg file
ansible --version
# note: any name is allow here cfg file name, xyz.cfg its okay also.
```

-   Second priority is currently working directory 

```sh
mkdir /home/raju/ansi_project
cd /home/raju/ansi_project 
touch ansible.cfg
ansible --version
# note: cfg file name mustbe ansible.cfg other name is not allow here
```

-   Third priority is user home directory 
-   create .ansible.cfg file in user home directory 

```sh
cd 
touch .ansible.cfg
ansible --version 
# note: cfg file name mustbe ansible.cfg other name is not allow here
```

-   Fourth priority default ansible cfg location 
-   if above three configuration is not there then default configuration is working 
-   default file location is /etc/ansible/ansible.cfg
