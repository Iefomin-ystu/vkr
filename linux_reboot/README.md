linux_reboot
=========

Перезапуск сервера.

Default Variables
------------
| Name                         | Type | Default value | Description                                                                                            |
|------------------------------|------|---------------|--------------------------------------------------------------------------------------------------------|
| _def_linux_reboot_force      | bool | false         | Принудительная перезагрузка                                                                            |
| _def_linux_post_reboot_delay | int  | 30            | Время, выжидаемое перед попыткой повторного подключения                                                |
| _def_linux_reboot_timeout    | int  | 300           | Максимальное время, в течение которого будут осуществляться попытки подключения к виртуальному серверу |


Role Parameters
------------
| Name                    | Type | Required | Value         | Description                                                                                            |
|-------------------------|------|----------|---------------|--------------------------------------------------------------------------------------------------------|
| linux_reboot_force      | bool | False    | [true, false] | Принудительная перезагрузка                                                                            |
| linux_post_reboot_delay | int  | False    | *             | Время, выжидаемое перед попыткой повторного подключения                                                |
| linux_reboot_timeout    | int  | False    | *             | Максимальное время, в течение которого будут осуществляться попытки подключения к виртуальному серверу |


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
- name: Linux - Reboot
  hosts: all
  roles:
    - role: tensor.linux.linux_reboot
      vars:
        linux_reboot_force: true
  collections:
    name: tensor.linux
```
