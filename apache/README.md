Role Name
=========

- HybridCloud05 Ansible Role - `apache`

Role Variables
--------------

**Variables**
- apache_listen: 80
- apache_name: "apache.example.com:{{ apache_listen }}"

- static_url: /static
- static_path: /data/monthly_challenges/staticfiles

- uvicorn_listen: 8000

- errorlog: /var/log/httpd/django_error.log
- accesslog: /var/log/httpd/django_access.log

Example Playbook
----------------

```
---
- name: 'Configuring apache'
  hosts: web01.hb05.local
  tasks:
    - name: 'Role - apache'
      ansible.builtin.include_role:
        name: apache
```