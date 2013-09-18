Ansible
=======

Prereq
------

Digital Ocean box running Arch Linux

Getting started
---------------

````
# copy all needed ssh keys to the DO box
ssh-copy-id -i ~/.ssh/id_rsa.pub root@146.185.138.175

# update Arch
pacman -Syy

# install python
pacman -S python2

# run a test (make sure your pwd is this repo)
ansible all -i hosts -m ping -u root
````

Todo
----
- add pacman -Syy to common task`
