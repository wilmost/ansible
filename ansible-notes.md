
## SSH keys

To generate a ssh key: 

- `ssh-keygen -t ed25519 `  

To copy sshkey:

`ssh-copy-id -i ~/.ssh/[key file] [user]@[ip of the destination server]`

 ssh-i <key path> [ip of the host] 

`eval $(ssh-agent)` -> to catch your passphrase in the background 


## Installing Ansible 

 
## ad-hoc commands 

- ansible all --key-file ~/.ssh/[key file] -i [inventory] -m ping

- ansible all --list-host ; shows a list of host defined in your inventory

- ansible all -m gather_facts

- ansible all -m gather_facts --limit [ip of a host]

    --become --ask-become-pass ; to elevate privileges

- ansible-playbook playbook.yml --list-hosts 


## ansible-playbook commands

 - ansible-playbook `myplaybook.yml` 

 - ansible-playbook myplaybook.yml --list-tasks ; is used to list all tasks that would be executed by a play without making any changes to the remote servers. 

 - ansible-playbook myplaybook.yml --list-hosts 

 - ansible-playbook myplaybook.yml --start-at-task="Set Up Nginx" 

 - ansible-playbook myplaybook.yml --tags=mysql,nginx




