wp-cli
=========

An Ansible role to install or update wp-cli.

Requirements
------------

There are no requirements in this role.

Role Variables
--------------

All variables come form the `defaults` directory. These can be overwiten by `group_vars/all.yml`. Here are the variables from this role.
* admin_home = By default this is set to the remote servers home directory.
* sub_dir = This variable is only used if you `bin` directory is elsewhere in the home directory.
* root_bin = This variable contains the whole path to the `bin` directory

Dependencies
------------

There are no Dependencies in this role. 

Files
-----
This role does not have any files related.

Handlers
--------
There are no handlers in this role.

Templates
--------------
There are no templates in this role.

Example Playbook
----------------

This is the most basic way to run the wp-cli playbook:
```
$ ansible-playbook wp-cli.yml
```
This command will only run tags set with "update":
```
$ ansible-playbook wp-cli.yml --tags update
```
This command will **only** display the hosts and tasks that would run with playlist. The wp-cli.yml playbook will not be run:
```
$ ansible-playbook wp-cli.yml --list-hosts --list-tasks
```

---

To make sure wp-cli is intalled and the version. Type the following command on the servers.
```
wp cli info
```

Or use the Ansible ad-hoc command.
```
ansible wordpress -i hosts -m shell -a "wp cli info"
```

---

## Server Commands

### WP-CLI
[wp-cli](http://wp-cli.org/) is a set of command-line tools for managing wp-cli installations. You can update plugins, configure multisite installs and much more, without using a web browser.
