richard-ansible
===============

Ansible playbook for deploying richard

I'll stop commiting directly to master once this gets in working shape.

* Create a server somewhere. be able to connect to it with sudo powers.
* edit inventory/development to point to your server.
* try running ./run.sh 

TODOs

The rackspace/ folder contains experiments on automating creation of
rackspace servers for people who run richard instances on rackspace.

I haven't got Vagrant working with ansible yet. I've been testing against
rackspace servers that I spin up for this.

I do not know how to generate a password for SECRET_KEY. I found
a snippet I am playing around with. It's not ready to be checked in.
for now the SECRET_KEY is set by hand in the roles/richard/defaults/main.yml file.

```
---
- hosts: localhost
  tasks:
    - local_action: shell openssl passwd -1 -in /dev/urandom | head -1
      register: secret_key
    - local_action: debug msg="secret_key is ${secret_key.stdout}"
```
