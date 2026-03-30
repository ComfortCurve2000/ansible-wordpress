WordPress
===========

This role installs WordPress on Debian 13.

The Backup/Restore functions have only had basic testing; make sure to thoroughly test with your site before relying on them.

Requirements
------------

No special modules are required.

Role Variables
--------------

vars/wordpress_vars.yml is a template for the required variables that should be copied and then configured in {{ inventory_dir }}/secure/

Dependencies
------------

Dependent on the system_base role.

Example Playbook
----------------
```
tasks:
  - name: Install system_base
    include_role:
      name: system_base
    tags: [system_base]

  - name: Install WordPress
    include_role:
      name: wordpress-debian
    tags: [wordpress]
```

License
-------

GPLv3

Author Information
------------------

Justin Mason