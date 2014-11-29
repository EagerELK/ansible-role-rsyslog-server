# Ansible Role: rsyslog

An Ansible Role that installs rsyslog.

## Requirements

None

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

~~~
rsyslog_server_udp: false
rsyslog_server_tcp: true
rsyslog_server_udp_port: 1514
rsyslog_server_tcp_port: 1514
rsyslog_server_folder: /var/syslog
~~~

The ports are set to 1514 due to a [bug in Ubuntu 12.04](https://bugs.launchpad.net/ubuntu/+source/rsyslog/+bug/789174) that prevents it from binding to a priviledged port.

## Dependencies

None

## Example Playbook

~~~
---
- hosts: all
  sudo: true
  roles:
    - syslog
~~~

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jrgns](http://jrgns.net), maintainer of [EagerELK](http://eagerelk.com).
