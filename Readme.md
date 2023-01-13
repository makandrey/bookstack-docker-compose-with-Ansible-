# Развертывание BookStack и Mattermost в Docker-Compose через Ansible

## В файле docker-compose.yml:
1. Задать имя сервера через переменную "APP_URL". Например: **APP_URL=http://192.168.0.71:80**. 
2. Задать учетные данные для БД.


## Создать виртуальное окружение Python и установить Ansible
```
cd bookstack-docker-compose-with-ansible
sudo apt update
sudo apt install python3-pip sshpass -y
sudo pip install virtualenv
virtualenv --version
sudo virtualenv -p python3 .
source ./bin/activate
sudo pip install ansible
```
## Запустить playbook от пользователя из группы sudo
```
ansible-playbook -i hosts -k -K playbook.yml 
```
