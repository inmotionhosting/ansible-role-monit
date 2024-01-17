![Ansible Molecule Pipeline](https://github.com/inmotionhosting/ansible-role-monit/actions/workflows/main.yml/badge.svg) [![GPL-3.0 License](https://img.shields.io/github/license/respheal/monit.svg?color=blue)](https://github.com/respheal/monit/blob/master/LICENSE)

![InMotion Hosting Ultrastack](https://www.inmotionhosting.com/wp-content/uploads/2024/01/ultrastack-logo-black-vertical.png)

# Ansible Role: Monit

Modular Ansible Role for deploying and configuring Monit

## Requirements
This Ansible role supports the two latest stable releases of specific
server-focused Linux distributions and aims to follow their deprecation
policies. Additionally we will focus on supporting the latest two stable
releases of each, which at the time of writing are as follows:

* CentOS 7.x
* Debian 10 or later
* Ubuntu 20.04 LTS or later
* AlmaLinux 8.x or later
* RockyLinux 8.x or later

## Dependencies

None.

## Role Variables

Available variables are listed below with their default values (you can also see `defaults/main.yml`)

| Variable | Description |
| -------- | ----------- |
| monit_daemon | Default: `monit`
| monit_executable_path | Default: `/usr/bin/monit`
| monit_config_dir | Default: `/etc/monit.d/`
| monitored_services | Default: `['httpd', 'mariadb', 'nginx', 'php-fpm', 'redis']`
| monit_systemd_restart | Default: `true`
| systemd_restart_setting | Default: `on-failure`

## Example Playbook

```yaml
- hosts: www
  roles:
    - role: monit
```

## License

GPLv3
