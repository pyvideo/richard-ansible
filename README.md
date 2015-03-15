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


Vagrant
=======

To use the Vagrant environment, do:

1. `pip install -r requirements.txt`
2. `vagrant up`

This uses Vagrant to create a vm with richard and its requirements set up.

You can connect to richard in the vagrant environment by pointing your
browser to `http://localhost:8000`.

Helpful commands:

* `vagrant up`: starts the environment
* `vagrant ssh`: sshs into the environment as the vagrant user
* `vagrant provision`: run ansible on the environment to pick up any
  configuration management changes
* `vagrant halt`: halts the environment
* `vagrant destroy`: destroys the vm
