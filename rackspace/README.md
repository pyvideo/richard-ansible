This directory has experiments where I try to figure out how to
automated things with Rackspace.

## Creating a rackspace server

* ssh public keys need to be in files/authorized_keys
* the RAX_CREDS_FILE environment variable should point to a rackspace credentials file
  as described http://docs.ansible.com/guide_rax.html#credentials-file

```
ansible-playbook -i rax_inventory -vv rax_create.yml 
```
## Deploying pyvideo

Currently I don't know how to get dynamic inventory working with
rackspace, (I'm  reviewing [rax_facts](http://docs.ansible.com/rax_facts_module.html) docs, meanwhile)
so you need to edit rax_inventory by hand to add the IP
of the server that you created.

Once you've done that. run

```
ansible-playbook -u root -i rax_inventory -vv site.yml
```
