Role Name
=========

This role installs and configures the WSUS role for Windows 2012 R2 and Windows 2016.

Requirements
------------

There are no special requirements apart from the standard items to allow Ansible to run on the target.

Role Variables
--------------

The following variables are defined in `/vars/main.yml`:
* `install_management_tools`: Whether to install the WSUS MMC or not.  Default is `yes`
* `content_folder`: Sets the folder location for WSUS to store its content.  Default is `C:\WSUS`
* `products_list`: A list of products which updates will be downloaded for.  Default items are `Windows Server 2012 R2` and `Windows Server 2016`
* `classification_list`: A list of the Update Classifications that will be enabled.  Default items are `Critical Updates` and `Security Updates`

Dependencies
------------

There are no known dependencies.

Example Playbook
----------------

An example playbook for using this role:

    - hosts: wsus_servers
      roles:
         - role: ansible-role-wsus

License
-------

MIT

Author Information
------------------
