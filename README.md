# Ansible Role: proxmox

[![Build Status](https://img.shields.io/travis/sbaerlocher/ansible.proxmox.svg?branch=master&style=popout-square)](https://travis-ci.org/sbaerlocher/ansible.proxmox) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-proxmox-blue.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/proxmox) [![Ansible Role](https://img.shields.io/ansible/role/d/35802.svg?style=popout-square)](https://galaxy.ansible.com/sbaerlocher/proxmox)

## Description

This is a role with which it is possible to configure Proxmox VE.

## Installation

```bash
ansible-galaxy install sbaerlocher.proxmox
```

## Requirements

None

## Role Variables

| Variable             | Default     | Comments (type)                                   |
| :---                 | :---        | :---                                              |
| proxmox_pveproxy_allow_from | ["127.0.0.1"] | |
| proxmox_pveproxy_cipers | ["ECDHE-ECDSA-AES256-GCM-SHA384","ECDHE-RSA-AES256-GCM-SHA384","ECDHE-ECDSA-CHACHA20-POLY1305","ECDHE-RSA-CHACHA20-POLY1305","ECDHE-ECDSA-AES128-GCM-SHA256","ECDHE-RSA-AES128-GCM-SHA256","ECDHE-ECDSA-AES256-SHA384","ECDHE-RSA-AES256-SHA384","ECDHE-ECDSA-AES128-SHA256","ECDHE-RSA-AES128-SHA256"] | |
| proxmox_pveproxy_deny_from | 'all' | |
| proxmox_pveproxy_policy | 'allow' | |
| proxmox_pve_iso | {"name": "ubuntu-server-18.04.1.0-x64","url": "http://releases.ubuntu.com/18.04.1.0/ubuntu-18.04.1.0-live-server-amd64.iso","state": "present"} | |

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
     - sbaerlocher.proxmox
```

## Changelog

### 1.0.0

* inital commit

## Author

* [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2019, Simon Bärlocher
