# Ansible role: systemd-journald
Logging

## Requirements
Only tested on Debian stable, for now.

## Role Variables
+ `journald_server`: where to upload journals to
+ `journald_port` (default: 19532): listener port for receiver (journald-remote)
+ `journald_iface` (default: primary network interface): bind listener to this interface
+ `journald_server_group` (default: log): inventory group on which to run journald-remote. All others that apply this role get journald-upload.

## Dependencies
None.

## Example Playbook

```
- hosts: linux
  roles:
    - { role: ho-ansible.systemd-journald }
```

## License
MIT

## Author Information
Ansible role by [Sean Ho](https://github.com/ho-ansible/)
