# ansible-openconnect

Install and configure openconnect client for vpns tunnels

## What does this ansible module do?

1. Installs the openconnect package from OS package sources
1. Creates directories on the filesystem
1. Creates a startup script for connecting to GP based VPNs

## Role Variables

Congfigure some variables for the GP startup script by adding these to your 
host_vars or group_vars.

```
openconnect_gp_vpn_endpoint: https://192.168.1.1
openconnect_gp_vpn_username: bwayne
openconnect_gp_csd_username: ansible
```
## Example Playbook

Applying the role to a group of servers while supplying the variables.

```
- hosts: servers
  roles:
    - role: ppouliot.openconnect
  vars:
    openconnect_gp_vpn_endpoint: https://192.168.1.1
    openconnect_gp_vpn_username: bwayne
    openconnect_gp_csd_username: bwayne
```
## Contributors

* Peter Pouliot 
  email: peter@pouliot.net

* David Karban
  email: david@karban.eu
  site: www.karban.eu

## License

* [GPLv2](./LICENSE)

## Contributors

* Peter Pouliot 
  email: peter@pouliot.net

* David Karban
  email: david@karban.eu
  site: www.karban.eu
