## Ansible role for systemd-networkd

***WORK IN PROGRESS -- ALPHA QUALITY***

This small Ansible role will take your current network configuration and create systemd-networkd network configuration files for you.  It will also prepare your system to use systemd-networkd and systemd-resolved after a reboot.

***It's not recommended to use this on an active production system unless you're really really sure that you want to use systemd-networkd.***

Also, this role currently supports:

* IPv4 addresses and gateways
* IPv6 addresses and gateways
* Additional IPv4 and IPv6 addresses
* Multiple network devices
* Devices with predictable names and those with old names

However, if you use complex networking, such as bonding, VLANs, VXLAN, or something else, this role isn't quite ready for you.

### Getting started

Edit the `hosts` file to contain the IP address of your host and then run:

    ansible-playbook -i hosts playbook.yml

The playbook only takes a few seconds to run.  Once it's done, reboot your server and cross your fingers for pings!

### Questions? Comments? Complaints?

All pull requests are welcomed. :)

*--Major*
