## Склонировать репозиторий в целевой каталог
```
git clone https://github.com/makandrey/bookstack-docker-compose-with-ansible.git
```
## Создать виртуальное окружение Python для Ansible
```
sudo apt install python3-pip -y
pip install virtualenv
virtualenv --version
virtualenv -p python3 <bookstack-docker-compose-with-ansible>
source <bookstack-docker-compose-with-ansible>/bin/activate
pip install ansible
```
## Запустить playbook
```
ansible-playbook 
```