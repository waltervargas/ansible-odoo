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
