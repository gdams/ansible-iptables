ansible-iptables
================

Iptables role for your playbook

# Supported platforms

* Ubuntu 14.04

# Usage

Example of playbook

Notice: `firewall` should be defined

```
- hosts: all
  user: root

  vars:
    - firewall:
        - { name: ssh, port: 22, ip: 0/0 }
        - { name: http, port: 80, ip: 0/0 }
        - { name: https, port: 443, ip: 0/0 }

  roles:
    - { role: iptables }
```
