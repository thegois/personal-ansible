# personal-ansible
Simple commands with ansible

## Inventory
It is necessary set hosts file as inventory in /etc/ansible/ansible.cfg.

## Security relationship
Ansible needs create a security relationship with target host, therefore it need to copy a ssh public key.

Ex: ssh-copy -i ~/.ssh/ira_rsa.pub user@server_host -p port.

After it is possible test a connection with ping module.

Ex: ansible <name_group> -m ping. 

If it returns green answer it dit work.
