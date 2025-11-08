Role Name
=========

- HybridCloud05 Ansible Role - `backup-client`

Role Variables
--------------

**Variables**
- backup_server: 172.16.6.76

- borg_user: borg
- borg_group: borg

- backup_dir: /data

**Secrets**
- user_password: borg

Example Playbook
----------------

```
---
- name: 'Set borgbakcup client'
  hosts: backup-client, localhost
  vars_files:
    - backup_password.yml
  tasks:
    - name: 'Role - backup-client'
      ansible.builtin.include_role:
        name: backup-client
```