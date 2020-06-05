# ansible-openconnect

Install and configure openconnect client for vpns tunnels

## What does this ansible module do?

1. Installs the openconnect package from OS package sources
1. Creates directories on the filesystem
1. Creates a startup script for connecting to GP based VPNs

https://github.com/ppouliot/ansible-openconnect
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

[GPLv2](./license)

## Copyright

    Copyright (C) 2020 Peter J. Pouliot

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.


## Contributors

* Peter Pouliot 
  email: peter@pouliot.net

* David Karban
  email: david@karban.eu
  site: www.karban.eu
