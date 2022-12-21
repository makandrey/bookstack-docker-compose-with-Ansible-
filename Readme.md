# Развертывание BookStack в Docker-Compose через Ansible

## В файле docker-compose.yml:
1. Задать имя сервера через переменную "APP_URL". Например: **APP_URL=http://192.168.0.71:80**. 
2. Задать учетные данные для БД.


## Создать виртуальное окружение Python и установить Ansible
```
cd bookstack-docker-compose-with-ansible
sudo apt install python3-pip sshpass -y
pip install virtualenv
virtualenv --version
virtualenv -p python3 .
source ./bin/activate
pip install ansible
```
## Запустить playbook от пользователя из группы sudo
```
ansible-playbook -i hosts -k -K playbook.yml 
```