
## SSH keys

To generate a ssh key: 

- `ssh-keygen -t ed25519 `  

To copy sshkey:

`ssh-copy-id -i ~/.ssh/[key file] [user]@[ip of the destination server]`

 ssh-i <key path> [ip of the host] 

`eval $(ssh-agent)` -> to catch your passphrase in the background 


## Installing Ansible 

 

ansible all --key-file ~/.ssh/[key file] -i [inventory] -m ping
