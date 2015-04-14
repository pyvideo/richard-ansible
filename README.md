richard-ansible
===============

Ansible playbook for deploying richard

* Create a server somewhere and be able to connect to it with sudo powers
* Edit inventory/development to point to your server
* Try running ./run.sh

To see a example of this playbook in use, refer to <https://github.com/pyvideo/pyvideo-deploy>. This is what deploys <http://pyvideo.org>.

Outstanding issues
==================

* See [issue list](https://github.com/pyvideo/richard-ansible/issues) for
  outstanding issues.


To use
======

1. Copy `vars/secret.yml-dist` to `vars/secret.yml` and put secret things
   in there. *This file should never be checked in.*
2. Copy `vars/all.yml-dist` to `vars/all.yml` and put site-specific
   configuration in there as well as override any variables you need
   to override. If you have no site-specific things, you can just
   leave it as is.
3. Create a virtual environment: `mkvirtualenv richardansible`
4. Install requirements: `pip install -r requirements.txt`


Using with Vagrant
==================

To use the Vagrant environment, do the above and then do:

1. `vagrant up`

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
