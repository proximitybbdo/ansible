BBDO goes Ansible
=================

Prereq
------

Digital Ocean box running **Arch Linux**

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

Troubleshooting
---------------

When generating password hashes for new users, it is important
that you use the same tool for the job both on the target
and local machine. E.g. when generating a password hash on
OSX and Arch using regular python crypt, it will fail to match.
Consider using http://stackoverflow.com/questions/15231661/how-do-i-create-a-user-and-set-a-password-using-ansible/17992126#17992126

Todo
----
- only create password on user creation, never overwrite
- oh-my-zsh folder -> chown to user:group (recursive)
- add node
- add grunt (global)
