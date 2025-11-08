Role Name
=========

- HybridCloud05 Ansible Role - `jenkins`

Requirements
------------

**Variables**
- source_src: https://pkg.jenkins.io/redhat-stable/jenkins.repo
- source_dest: /etc/yum.repos.d/jenkins.repo 
- rpm_key: https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

- jenkins_port: 8080
- java_path: /usr/lib/jvm/java-21-openjdk-21.0.8.0.9-1.el9.x86_64/bin/java


Example Playbook
----------------

```
---
- name: 'Install jenkins'
  hosts: jenkins
  tasks:
    - name: 'Role - jenkins'
      ansible.builtin.include_role:
        name: jenkins
```
