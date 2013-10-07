Ansible
=======

Prereq
------

Digital Ocean box running Arch Linux

Getting started
---------------

````
[remote]

# update Arch
pacman -Syy

# install python
pacman -S python2

[local]
# run a test (make sure your pwd is this repo)
ansible all -i hosts -m ping -u root
````
