# Install ansible in RHEL 9 

-   update your OS
```sh
dnf install -y epel-release
dnf update
```
### Install ansible core 

-   By default ansible core install 
```sh
dnf install ansible-core -y
dnf install -y ansible
ansible --version   ## ansible version 
ansible-doc -l  ## ansible modules
ansible-doc -l | wc -l  ## ansible modules list 
```

### Install ansible with pip 

-   You can install ansible with python pip and its install more module then ansible core 
-   For new version python3 is not working so install 3.12 version and used it 

```sh
dnf install curl -y
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py         ## download pip 
python3 -m pip -V       ## see pip version 
python3 get-pip.py --user
python3 -m pip install --user ansible           ## install ansible 
export PATH=$PATH:~/.local/bin                  ## For permanent used bash_profile 
ansible --version   ## ansible version 
ansible-doc -l  ## ansible modules
ansible-doc -l | wc -l  ## ansible modules list 
```
