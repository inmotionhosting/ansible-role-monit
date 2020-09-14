[![Build Status](https://travis-ci.org/respheal/monit.png?branch=master)](https://travis-ci.org/respheal/monit) [![GPL-3.0 License](https://img.shields.io/github/license/respheal/monit.svg?color=blue)](https://github.com/respheal/monit/blob/master/LICENSE)

# Ansible Role: Monit

Modular Ansible Role for deploying and configuring Monit

## Requirements

* CentOS 7.x or later
* Debian 9 or later
* Ubuntu 16.04 LTS or later

## Dependencies

None.

## Role Variables

Available variables are listed below with their default values (you can also see `defaults/main.yml`)

| Variable | Description |
| -------- | ----------- |
| monit_config_dir | Default: `/etc/monit.d/`
| monitored_services | Default: `['httpd', 'mariadb', 'nginx', 'php-fpm', 'redis']`

## Example Playbook

```yaml
- hosts: www
  roles:
    - role: monit
```

## License

GPLv3
