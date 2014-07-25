## Odoo (OpenERP) 8 Ansible Playbooks

### Setup dev enviroment

1. Run vagrant up
2. Run ansible-playbook setup.yml
 
   ```sh
$ ansible-playbook -c paramiko -i develop setup.yml --ask-pass --sudo
```

3. Run ansible-playbook site.yml

   ```sh
$ ansible-playbook -i develop site.yml 
```

### Description by components

#### Vagrant

Vagrant file features:

 - IP Address: 192.168.33.2
 - Share ../addons folder with odoo local addons path (Make this folder before run)
 - Share ~/git/odoo folder to /opt/odoo (Clone odoo here before run)

#### Postgres Role

Postgres role features:

 - Install postgresql 9.3 from http://apt.postgresql.org/pub/repos/apt/
 - Create openerp role in postgresql
 
#### Nginx Role
 
Postgres role features:
 
  - Install nginx
