# Install ansible in RHEL 9 

-   update your OS
```sh
dnf update -y
```
### install ansible core 

-   By default ansible core install 
```sh
dnf install ansible-core -y
ansible --version   ## ansible version 
ansible-doc -l  ## ansible modules
ansible-doc -l | wc -l  ## ansible modules list 
```

### Install ansible with pip 

-   You can install ansible with python pip and its install more module then ansible core 

```sh
dnf install curl -y
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py         ## download pip 
python3 -m pip -V       ## see pip version 
python3 get-pip.py --user
python3 -m pip install --user ansible           ## install ansible 
ansible --version   ## ansible version 
ansible-doc -l  ## ansible modules
ansible-doc -l | wc -l  ## ansible modules list 
```
