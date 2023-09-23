Ansible Apache<br/>[![Push to Galaxy](https://github.com/MozkaGit/ansible-role-apache/actions/workflows/push_to_galaxy.yml/badge.svg)](https://github.com/MozkaGit/ansible-role-apache/actions/workflows/push_to_galaxy.yml)
=========

This Ansible role lets you deploy an Apache server.

Requirements
------------

- Ansible 2.1 or later.
- The target host must be CentOS, as the role installs the EPEL repository for CentOS.

Role Variables
--------------

Here are the variables available to customize this role:

- system_user: System user (default: vagrant).
- container_name: Container name (default: apache).
- exposed_ports: Exposed ports (default: 80:80).
- bind_mount: Bind mount (default: /home/vagrant/index.html:/usr/local/apache2/htdocs/index.html).
- template_dest: Template destination (default: /home/vagrant/index.html).
- credentials_vault_file_dest: Destination of credentials vault file (default: roles/ansible-apache-role/files/secrets/credentials.vault).

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible-apache-role

License
-------

MIT / BSD

Author Information
------------------

This role was created by MozkaGit.
