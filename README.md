![Ansible Lint](https://github.com/johanneskastl/ansible-role-glusterfs_servers/workflows/Ansible%20Lint/badge.svg)

glusterfs_servers
=========

Configure glusterfs servers

Requirements
------------

None.

Role Variables
--------------

Optional variables:

- `force_ipv4_as_ipv6_not_available`: (Boolean) In case your machines do not
  have working IPv6 or DNS (or `/etc/hosts`) only return IPv4 addresses, you can
  force the usage of IPv4 for the server side by setting this to `true`

Internally used variables:

There are some variables that are used internally, as they are OS-related. These
are loaded from the files in `vars/` automatically, currently for Debian and
openSUSE only.

These variables are:

- `glusterfs_packages`: (String) list of packages to install
- `glusterfs_server_service`: (String) name of the systemd unit for glusterd

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: 'johanneskastl.glusterfs_servers'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
