Коллекция Ansible с тестовой ролью, использующей тестовый модуль
=========
Описание
---
В данной коллекции *my_own_collection* реализована роль *my_own_role*, которая использует кастомный модуль *my_own_module*, который в свою очередь записывает в файл по пути *path* содержимое, указанное в параметре *contetnt*.

```
PLAY [all] ***********************************************************************

TASK [Gathering Facts] ***********************************************************************
ok: [ubuntu_clean]

TASK [my_own_namespace.my_own_collection.my_own_role : run my own module] ***********************************************************************
changed: [ubuntu_clean]

PLAY RECAP ***********************************************************************
ubuntu_clean               : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

#повторный запуск для проверки идемпотентности#

PLAY [all] ***********************************************************************

TASK [Gathering Facts] ***********************************************************************
ok: [ubuntu_clean]

TASK [my_own_namespace.my_own_collection.my_own_role : run my own module] ***********************************************************************
ok: [ubuntu_clean]

PLAY RECAP ***********************************************************************
ubuntu_clean               : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

```

Тест для установки коллекции из архива тут:
---
https://github.com/OlegAnanyev/my_own_collection/tree/master/!test

