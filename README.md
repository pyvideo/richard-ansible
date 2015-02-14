richard-ansible
===============

Ansible playbook for deploying richard

I'll stop commiting directly to master once this gets in working shape.

The rackspace/ folder contains experiments on automating creation of
rackspace servers for people who run richard instances on rackspace.

TODOs

I do not know how to generate a password for SECRET_KEY. I found
a snippet I am playing around with. It's not ready to be checked in.

```
---
- hosts: localhost
  tasks:
    - local_action: shell openssl passwd -1 -in /dev/urandom | head -1
      register: secret_key
    - local_action: debug msg="secret_key is ${secret_key.stdout}"
```
