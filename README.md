BBDO goes Ansible
=================

Prereq
------

- Digital Ocean box running **Arch Linux**
- Ansible 1.3 (update_password option for the user module)

Getting started
---------------

````
[remote]

# update Arch
pacman -Syy

# install python
pacman -S python2

# or in a gist form
sudo bash -c 'bash <( curl -s https://gist.github.com/pierot/7066699/raw/d7c7b934e2dab02ab3bdac978714c106fa7929d6/arch_for_ansible)'

[local]
# make sure you can ssh without password
ssh-copy-id -i ~/.ssh/id_rsa.pub root@XXX

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
