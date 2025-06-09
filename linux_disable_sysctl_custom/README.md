linux_disable_sysctl_custom
=========

Удаление всех кастомных настроек ядра через sysctl и возвращение к default.

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
- name: Linux - Disable all custom sysctl confinguration
  hosts: all
  roles:
    - tensor.linux.linux_disable_sysctl_custom
  collections:
    name: tensor.linux
```
