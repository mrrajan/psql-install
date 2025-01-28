# psql-install

Ansible-playbook to install PSQL on given host

## Requirements
 - Ansible 2.16.0 or greater

## Provision
Update the contents on `hosts.yaml` file
```

---
trustification:
  vars:
    ansible_ssh_private_key_file: # Location to the private keys
  children:
    rhel:
      hosts:
        slaves-ansible:
          ansible_host: # IP address of the VM
      vars:
        ansible_ssh_user: # User name for SSH

```
## Installation
Run the playbook with the command
```
ansible-playbook -i hosts.yaml  play.yaml
```
This will create `postgres` database under localhost.