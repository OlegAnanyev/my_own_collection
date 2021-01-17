Установить коллекцию из архива и запустить плейбук, использующий роль из данной коллекции:
```
ansible-galaxy collection install my_own_namespace-my_own_collection-1.0.0.tar.gz
ansible-playbook -i inventory/prod.yml --ask-pass --ask-become-pass playbook.yml
```