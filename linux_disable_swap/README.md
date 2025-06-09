linux_disable_swap
=========

Отключение swap на сервере. Добавление освобожденного дискового пространства в корневой раздел.

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
- name: Linux - Disable Swap
  hosts: all
  roles:
    - tensor.linux.linux_disable_swap
  collections:
    name: tensor.linux
```
