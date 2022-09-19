# CyberEd-HacherU-module2-lab1
Лабораторная работа по реализации кластера серверов Ubuntu с помощью Vagrant и их конфигурированию с помощью Ansible.

**Полезные команды:**
- vagrant box add _$box-file_ --name _$box-name_
- vagrant init
- vagrant box list
- vagrant up
- vagrant status
- vagrant destroy
- vagrant ssh _$vm-name_
- ansible -i _$inventory-file_ _$main-file_ -m ping
- ansible-vault create _$encrypted-credentials-file_
- ansible-playbook -i _$inventory-file_ _$main-file_ -D --ask-vault-pass --extra-vars '@_$encrypted-credentials-file_'
