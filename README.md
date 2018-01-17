Role Name
=========

Ansible role to install boinc-client on remote machine.
I will also configure your machine as allowed to connect to via rpc and set a rpc password.
Check out the default variable to understand how to override this.

Requirements
------------

Ubuntu 16
Fedora 27

Role Variables
--------------

```
# Boinc password to connect via rpc
boinc_password: "boincpassword"

# List of remote hosts allowed to connect via rpc
boinc_remote_host_ips:
  - "{{ hostvars['localhost']['ansible_default_ipv4']['address'] }}"

# RPC port
boinc_rpc_port: "31416"
```

Dependencies
------------

None

Example Playbook
----------------

```
    - hosts: servers
      vars:
        boinc_password: "mydifferentpassword"
        boinc_rpc_port: 8888
      roles:
         - boinc-client
```

License
-------

MIT

Author Information
------------------

Albert Mikaelyan - tahvok at gmail dot com
