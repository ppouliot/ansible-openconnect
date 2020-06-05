# ansible-openconnect

Install and configure openconnect client for vpns tunnels

## Requirements

Any pre-requisites that may not be covered by Ansible itself or the role
should be mentioned here. For instance, if the role uses the EC2 module,
it may be a good idea to mention in this section that the boto package
is required.

## Role Variables

A description of the settable variables for this role should go here, including
any variables that are in defaults/main.yml, vars/main.yml, and any variables that
can/should be set via parameters to the role. Any variables that are read from other
roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned
here as well.

## Dependencies

A list of other roles hosted on Galaxy should go here, plus any details in regards
to parameters that may need to be set for other roles, or variables that are used
from other roles.

## Example Playbook

### configure the global protect script.

Congfigure some variables for the GP startup script by adding these to your 
host_vars or group_vars.

```
openconnect_gp_vpn_endpoint: 'https://192.168.1.1'
openconnect_gp_vpn_username: bwanyne
openconnect_gp_csd_username: ansible
```
### Applying the role to a group of servers

```
- hosts: servers
  roles:
    - role: ppouliot.openconnect
  vars:
    openconnect_gp_vpn_endpoint: 'https://192.168.1.1'
    openconnect_gp_vpn_username: bwanyne
    openconnect_gp_csd_username: ansible
```

## Contributors

* Peter Pouliot 
  email: peter@pouliot.net
* David Karban
  email: david@karban.eu
  site: www.karban.eu

## License

[GPLv2](./license)
