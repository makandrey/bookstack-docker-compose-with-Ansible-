## Склонировать репозиторий в целевой каталог
```
git clone https://github.com/makandrey/bookstack-docker-compose-with-ansible.git
```
## Создать виртуальное окружение Python для Ansible
```
cd bookstack-docker-compose-with-ansible
sudo apt install python3-pip -y
pip install virtualenv
virtualenv --version
virtualenv -p python3 .
source ./bin/activate
pip install ansible
sudo apt install sshpass
```
## Запустить playbook от пользователя из группы sudo
```
ansible-playbook -i hosts -k -K playbook.yml 
```