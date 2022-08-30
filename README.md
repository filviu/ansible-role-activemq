# Ansible Role: Apache ActiveMQ

[![CI](https://github.com/silviuvulcan/ansible-role-activemq/workflows/CI/badge.svg?event=push)](https://github.com/silviuvulcan/ansible-role-activemq/actions?query=workflow%3ACI)

Sets up Apache ActiveMQ from binary tgz.

## Requirements

None.

## Role Variables

Interesting variables are listed below, along with default values (see `defaults/main.yml` for a full list):

    activemq_version: 5.15.13

The version you wish to install. It also impacts the installation path.

    activemq_install_path: /opt

Path under which to install activemq. It will be `/SOME_PATH/apache-activemq-x.yy.z`

    activemq_user: apachemq
    activemq_group: apachemq

User and group under which to setup files and start activemq.

    activemq_force_install: false

Unless this is true the role will not overwrite if the path already exists.

## Dependencies

None.

## Example Playbook

```yaml
---
- hosts: all

  roles:
    - filviu.activemq
      activemq_version: 5.15.13
      activemq_install_path: /opt
      activemq_user: activemq
      activemq_group: activemq
      activemq_config_template: activemq.xml.j2
```

## License

MIT / BSD


## Author Information

This role was created by Silviu Vulcan to scratch his own itch.
