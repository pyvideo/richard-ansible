richard-ansible
===============

Ansible playbook for deploying richard

* Create a server somewhere and be able to connect to it with sudo powers
* Edit inventory/development to point to your server
* Try running ./run.sh


Outstanding issues
==================

* See [issue list](https://github.com/pyvideo/richard-ansible/issues) for
  outstanding issues.


Using with Vagrant
==================

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
