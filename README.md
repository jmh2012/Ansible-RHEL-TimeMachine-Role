# Ansible macOS Time Machine server Role

Ansible role to configure a  macOS Time Machine server on RHEL7/CentOS7 based hosts.

## Setting a time machine user password var
Passwords passed to the Ansible user module need to be pre-hashed. This command can generate the hash:
```
ansible all -i localhost, -m debug -a "msg={{ 'mypassword' | password_hash('sha512', 'mysecretsalt') }}"
```


