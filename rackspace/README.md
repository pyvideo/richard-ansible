This directory has experiments where I try to figure out how to
automated things with Rackspace.

If you use the cloud control server panel to create a server, ignore this.

## Creating a rackspace server

* ssh public keys need to be in files/authorized_keys
* the RAX_CREDS_FILE environment variable should point to a rackspace credentials file
  as described http://docs.ansible.com/guide_rax.html#credentials-file

Create a server by running the rax_create.yml file.

```
ansible-playbook -i rax_inventory -vv rax_create.yml 
```

Once you creat this, you'll have the ip you can use in inventory with the richard playbook.


## Deploying pyvideo

Currently I don't know how to get dynamic inventory working with
rackspace, (I'm  reviewing [rax_facts](http://docs.ansible.com/rax_facts_module.html) docs, meanwhile)
so you need to edit the richard playbook inventory by hand to add the IP
of the server that you created.
