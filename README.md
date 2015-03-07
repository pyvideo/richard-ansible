richard-ansible
===============

Ansible playbook for deploying richard

* Create a server somewhere. be able to connect to it with sudo powers.
* edit inventory/development to point to your server.
* try running ./run.sh 

TODOs

* The rackspace/ folder contains experiments on automating creation of
  rackspace servers for people who run richard instances on rackspace.
* I haven't got Vagrant working with ansible yet. Please track 
  [#4](https://github.com/pyvideo/richard-ansible/issues/4) if this affects you.
* I do not know how to generate a password for SECRET_KEY. Please track 
  [#5](https://github.com/pyvideo/richard-ansible/issues/4) if this affects you.
