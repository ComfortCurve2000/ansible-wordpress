# ansible-wordpress
This repository serves as an introduction to Ansible by deploying WordPress. The requirements are that you have a Debian 13 minimal installation with SSH working, and ansible installed on your workstation. Depending on your configuration, you may find the ansible-playbook flags `-k` and `-K` useful.

See README.md under each role. Playbooks live under their respective roles. Create a folder in this directory called `secure` to hold your configured variables, .gitignore should prevent it from being synchronized with github.

After configuring hosts and your wordpress_vars, here is the main playbook:

`ansible-playbook roles/wordpress-debian/build-wordpress.yml -e @secure/variables/wordpress_vars.yml`

The Backup/Restore functions have only had basic testing; make sure to thoroughly test with your site before relying on them.