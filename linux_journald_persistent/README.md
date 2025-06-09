linux_journald_persistent
=========

Приведение параметров systemd-journald c настройками постоянного хранения.

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
- name: Linux - Set systemd-journald storage to persistent
  hosts: all
  roles:
    - tensor.linux.linux_journald_persistent
  collections:
    name: tensor.linux
```
