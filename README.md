# personal-ansible
A personal ansible commands.

## Inventory
It is necessary set hosts file as inventory in /etc/ansible/ansible.cfg.

## Security relationship
Ansible needs create a security relationship with target host, therefore it needs to copy a ssh public key.

Ex: ssh-copy -i ~/.ssh/ira_rsa.pub user@server_host -p port.

After it is possible test a connection with ping module.

Ex: ansible <name_group> -m ping. 

If it returns green answer it did work.

## Roles
This project use roles structure, therefore it was added one main role: common-role. Each role will be responsible for specific informations such as: files, tasks or varibles. 
It was created by ansible-galaxy init <<name_role>>

## Tasks
Developed tasks:
  copy-log: Easy way to copy files from servers. (common-role)
