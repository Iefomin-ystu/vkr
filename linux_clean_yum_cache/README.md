linux_clean_yum_cache
=========

Очистка кэша yum/dnf.

Limitations
------------

На данный момент роль работает с операционными системами:

- CentOS/RedHat
    - 7.X
    - 8.X
    - 9.X
- AlmaLinux
    - 9.X
- RedOS
    - 7.3.2

Example Playbook
----------------

```yaml
---
- name: Linux - Clean yum cache
  hosts: all
  roles:
    - tensor.linux.linux_clean_yum_cache
  collections:
    name: tensor.linux
```
