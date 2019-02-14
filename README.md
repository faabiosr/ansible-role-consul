# Ansible Role: Consul
[![Build Status](https://img.shields.io/travis/fabiorphp/ansible-role-consul/master.svg?style=flat-square)](https://travis-ci.org/fabiorphp/ansible-role-consul)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://github.com/fabiorphp/ansible-role-consul/blob/master/LICENSE)

An ansible role to install and configure Consul agent.

## Requirements
None

## Role Variables
Please look at the [defaults/main.yml](defaults/main.yml) to see all default variables.

```yml
---
consul_config:
  server: true
  data_dir: "/var/consul"
  ui: true
```
The mandatory variable is the `consul_config`, this dict is composed by [Consul options](https://www.consul.io/docs/agent/options.html).

## Dependencies
None.

## Example Playbook

```yml
---
- name: "Consul server"
  hosts: servers
  vars:
    # Consul
    consul_config:
      server: true
      datacenter: brazil-01
      data_dir: "/var/consul"
      bind_addr: "{{ ansible_default_ipv4.address }}"
      ui: true
      client_addr: "0.0.0.0"

  roles:
    - role: fabiorphp.consul
```

## Author Information
This role was created in 2019 by [Fábio Ribeiro](https://github.com/fabiorphp).
