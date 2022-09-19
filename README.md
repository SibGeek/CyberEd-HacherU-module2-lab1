# CyberEd-HacherU-module2-lab1
Лабораторная работа по реализации кластера серверов Ubuntu с помощью Vagrant и их конфигурированию с помощью Ansible.

**Полезные команды:**
- ```vagrant box add $box-file --name $box-name```
- ```vagrant init```
- ```vagrant box list```
- ```vagrant up```
- ```vagrant status```
- ```vagrant destroy```
- ```vagrant ssh $vm-name```
- ```ansible -i $inventory-file $main-file -m ping```
- ```ansible-vault create $encrypted-credentials-file```
- ```ansible-playbook -i $inventory-file $main-file -D --ask-vault-pass --extra-vars '@$encrypted-credentials-file'```
