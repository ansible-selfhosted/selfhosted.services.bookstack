[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border.json)](https://github.com/copier-org/copier)
[![Podman Badge](https://img.shields.io/badge/Podman-892CA0?logo=podman&logoColor=white)](https://podman.io/)
[![Hatch project](https://img.shields.io/badge/%F0%9F%A5%9A-Hatch-4051b5.svg)](https://github.com/pypa/hatch)
![CI](https://github.com/ansible-selfhosted/selfhosted.services.bookstack/actions/workflows/ci.yml/badge.svg)
[![Ansible](https://img.shields.io/badge/Ansible-Molecule-EE0000?style=plastic&logo=ansible&logoColor=white)](https://github.com/ansible/molecule)

<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: [bookstack](https://www.bookstackapp.com/docs/)

A role to deploy Bookstack using rootless Podman with systemd.

## Role Requirements

- none

*Refer to services collection for general requirements*

## Role Arguments

|Option|Description|Type|Required|Default|
|---|---|---|---|---|
|bookstack_app_key|The application key for Bookstack.<br>Generated if not provided.<br>Can be generated using <code>echo "base64:$( dd if=/dev/urandom bs=1 count=32 status=none &#124; base64)"</code>|str|False|<auto_generated>|
|bookstack_config_path|The path for the Bookstack config.|str|False|~/.config/bookstack/|
|bookstack_db_config_path|The path for the Bookstack database config.|str|False|~/.config/bookstack-db/|
|bookstack_db_data_path|The path for the Bookstack database data.|str|False|~/.local/share/containers/storage/bookstack-db/|
|bookstack_timezone|The timezone for the bookstack service.|str|False|Etc/UTC|
|bookstack_web_port|The default port for the web server.|int|False|8080|


## Example Playbook

```
- hosts: all
  tasks:
    - name: Importing bookstack role
      ansible.builtin.import_role:
        name: selfhosted.services.bookstack
      vars:
```

## License

This project is licensed under the [MIT License](LICENSE)


⊂(▀¯▀⊂)

<!-- END_ANSIBLE_DOCS -->
