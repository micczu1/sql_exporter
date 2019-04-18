**Obsolete.
Current is here: https://github.com/micczu1/sql_exporter1 (wrapped up different implementation of sql_exporter)**


# Ansible Role: sql_exporter

## Description

Ansible role for install Prometheus sql_exporter that runs user-defined SQL queries at flexible intervals and exports the resulting metrics via HTTP for Prometheus consumption.

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `sql_exporter_version` | 0.2.0 | sql_exporter package version. |
| `sql_exporter_web_listen_address` | "0.0.0.0:9237" | Address on which sql_exporter will listen |
| `sql_exporter_config_dir` | /etc/sql_exporter | |

### Playbook

Use it in a playbook as follows:

```yaml
- hosts: all
  become: yes
  roles:
    - sql_exporter
```

## Configuration notes

Some helpful tips are in original sql_exporter [README.md](https://github.com/justwatchcom/sql_exporter/blob/master/README.md):  
https://github.com/justwatchcom/sql_exporter/blob/master/README.md

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.

This role is inspired by https://github.com/cloudalchemy/ansible-mysqld-exporter  
Sql_exporter is created by: https://github.com/justwatchcom/sql_exporter and this is only wrap-up in Ansible role.
