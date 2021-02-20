# Instalação zabbix-server 5.0 usando ansible AWS

![Badge](https://img.shields.io/badge/ansible-zabbix-red)

## Dependências
![Badge](https://img.shields.io/badge/ansible-2.9.10-blue)
![Badge](https://img.shields.io/badge/CentOS-7-blue)

## Edite o arquivo hosts para ip do host destino

## Exemplo de playbook
```
---
- name: Install Zabbix Server
  hosts: all
  vars:
    zbx_database_address: 127.0.0.1
    zbx_database_password: m19ScDhGljKI#!
    mysql_port: 3306
    pass_zabbix: zabbix2020
  become: yes
  roles:
  - zabbix-server
  
ansible-playbook -i hosts zabbix.yml
``` 
## Licença
![Badge](https://img.shields.io/badge/license-GPLv3-green)