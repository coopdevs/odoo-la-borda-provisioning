# Ansible inventories
This repository stores hosts informations and related variables for this specific instance of Odoo.

## Requirements

1. Clone this repo and [odoo-provisioning](https://gitlab.com/femprocomuns/odoo-provisioning) in the same directory
2. Go to `odoo-provisioning` directory and install Ansible dependencies:
   ```
   ansible-galaxy -r requirements.yml
   ```
3. Setup system administrators pointing to the `inventory/hosts` file of this repository:
   ```
   ansible-playbook playbooks/sys_admins.yml -i ../odoo-la-borda-provisioning/inventory/hosts --limit=dev
   ```
4. Run `provision.yml` playbook pointing to the `inventory/hosts` file of this repository:
   ```
   ansible-playbook playbooks/provision.yml -i ../odoo-la-borda-provisioning/inventory/hosts --ask-vault-pass --limit=dev
   ```
