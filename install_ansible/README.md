# Install ansible in RHEL 9 

-   update your OS
```sh
dnf update -y
```
### Install ansible core 

-   By default ansible core install
```sh
dnf install ansible-core -y
ansible --version   ## ansible version 
ansible-doc -l  ## ansible modules
ansible-doc -l | wc -l  ## ansible modules list 
```

### Install ansible with pip 

-   You can install ansible with python pip and its install more module then ansible core
-   Python version 3 not working in RHEL 8.10 so used 3.12
-   First install python 3.12 or higher 

```sh
dnf install curl -y
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py         ## download pip 
python3 -m pip -V       ## see pip version 
python3 get-pip.py --user
python3 -m pip install --user ansible           ## install ansible
export PATH=$PATH:~/.local/bin      ## for permanent used bash_profile
ansible --version   ## ansible version 
ansible-doc -l  ## ansible modules
ansible-doc -l | wc -l  ## ansible modules list 
```
