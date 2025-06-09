linux_configure_tuned
=========

Активация профиля tuned.

Default Variables
------------

| Name                             | Type   | Default value            | Description                                    |
|----------------------------------|--------|--------------------------|------------------------------------------------|
| _def_default_tuned_profiles_list | list   | ['balanced','desktop','hpc-compute','latency-performance','network-latency','network-throughput','powersave','throughput-performance','virtual-guest','virtual-host'] | Список стандартных профилей tuned |
| _def_custom_tuned_profiles_list  | list   | ['postgresql-db', 'dpc-vm', 'clickhouse', 'secure-postgresql-db', 'secure-dpc-vm', 'secure-clickhouse', 'ceph'] | Список поддерживаемых кастомных профилей tuned |
| _def_linux_tuned_profile         | string | dpc-vm                      | Стандартный профиль tuned                      |


Role Parameters
------------
| Name          | Type   | Required | Value | Description                  |
|---------------|--------|----------|-------|------------------------------|
| linux_tuned_profile | string | False    | ['balanced','desktop','hpc-compute','latency-performance','network-latency','network-throughput','powersave','throughput-performance','virtual-guest','virtual-host', 'postgresql-db', 'dpc-vm', 'clickhouse', 'secure-postgresql-db', 'secure-dpc-vm', 'secure-clickhouse', 'ceph'] | Профиль tuned для активации  |

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
- name: Linux - Configure Tuned
  hosts: all
  roles:
    - role: tensor.linux.linux_configure_tuned
      vars:
        linux_tuned_profile: postgresql-db
  collections:
    name: tensor.linux
```
