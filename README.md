[![Build Status](https://travis-ci.com/calvinbui/ansible-datadog.svg?branch=master)](https://travis-ci.com/calvinbui/ansible-datadog)
![GitHub release](https://img.shields.io/github/release/calvinbui/ansible-datadog.svg)
![Ansible Quality Score](https://img.shields.io/ansible/quality/40820.svg)
![Ansible Role](https://img.shields.io/ansible/role/d/40820.svg)

# Ansible Datadog Agent

Install and configure the Datadog agent

##  Requirements

N/A

## Role Variables

`datadog_api_key`: API Key

`datadog_user`: User the datadog agent runs as

`datadog_groups`: Groups to add the datadog user to

`datadog_integrations`: A dictionary of all the integrations to install and their contents


## Dependencies

N/A

## Example Playbook

```yaml
- hosts: servers
  become: true
  pre_tasks:
    - name: Update apt cache.
      apt:
        update_cache: true
        cache_valid_time: 600
      changed_when: false
  roles:
   - role: calvinbui.ansible_datadog
```

## License

GPLv3

## Author Information

http://calvin.me
