Коллекция Ansible с тестовой ролью, использующей тестовый модуль
=========
Описание
---
В данной коллекции *my_own_collection* реализована роль *my_own_role*, которая использует кастомный модуль *my_own_module*, который в свою очередь выводит сообщение *Hasta la vista, baby* на любое значение параметра *name*.

```
PLAY [all] *************************************************

TASK [Gathering Facts] *************************************
ok: [ubuntu_clean]

TASK [my_own_role : run my own module] *********************
changed: [ubuntu_clean]

TASK [my_own_role : dump test output] **********************
ok: [ubuntu_clean] => {
    "msg": {
        "changed": true,
        "failed": false,
        "message": "Hasta la vista, baby",
        "original_message": "hello!"
    }
}

PLAY RECAP *************************************************
ubuntu_clean               : ok=3    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```

Тест для установки коллекции из архива тут:
---
https://github.com/OlegAnanyev/my_own_collection/tree/master/!test

