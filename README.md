# Ansible Role: Self-signed SSL Certificate
Role for generating self-signed SSL certificates.

## Requirements
None.

## Role Variables
Available variables are listed below, along with their default values.

```yaml
self_signed_ssl_hosts: []
```
A list of hosts to generate self-signed SSL certificates for. Certificates are stored in the `/etc/ssl/self-signed-certs` directory. 

## Dependencies
None.

## Example Playbook
```yaml
- hosts: server
  become: yes

  vars:
    self_signed_ssl_hosts:
    - ansible.com
    - example.com

  tasks:
  - import_role:
      name: damianlewis.self_signed_ssl
```

## License
MIT

## Author
Damian Lewis