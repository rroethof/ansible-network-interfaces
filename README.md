Ansible Network Interfaces
==========================

This is an Ansible role that manages network interface configuration on Debian/Ubuntu servers


Requirements
------------

 * Ubuntu 12.04
 * Ubuntu 14.04


Dependencies
------------

none


Example Playbook
----------------

```yml
- hosts: all
  sudo: true
  sudo_user: root

  roles:
  - role: network-interfaces

```

```yml
network_manage_devices: yes
network_interfaces:

  - device: eth0
    description: static interface
    auto: true
    family: inet
    method: static
    address: 192.168.122.151
    network: 192.168.122.0
    netmask: 255.255.255.0
    gateway: 192.168.122.1
    nameservers:
    - 8.8.8.8
    - 8.8.4.4

  - device: eth1
    description: dhcp interface
    auto: true
    family: inet
    method: dhcp
```


License
-------

GPLv3


Author Information
------------------

Ronny Roethof 2015
