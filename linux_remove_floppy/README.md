linux_remove_floppy
=========

Удаление Floppy устройства.

Limitations
------------
Для окончательного применения необходимо перезагрузить операционную систему.

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
- name: Linux - Remove Floppy
  hosts: all
  roles:
    - tensor.linux.linux_remove_floppy
  collections:
    name: tensor.linux
```
