# deploy-zabbix-server-ansible
deploy zabbix server on ubuntu 22.04 with ansible



# Ansible Playbook for Installing Zabbix Server

This Ansible playbook automates the installation and configuration of Zabbix Server on Ubuntu 22.04. Zabbix is an open-source monitoring solution that allows you to monitor various network services, servers, and other resources.

## Prerequisites

Before using this playbook, make sure you have the following prerequisites:

Ansible Installed
Ensure Ansible is installed on the machine from which you plan to run this playbook. You can install Ansible using the following command:

   ```shell
   sudo apt-get update
   sudo apt-get install ansible

Inventory File
Create an Ansible inventory file (e.g., inventory.ini) containing the target server(s) where you want to install Zabbix Server. Here's an example of an inventory file:

[servers]
server_ip ansible_ssh_user=your_ssh_user ansible_ssh_pass=your_ssh_password


Replace server_ip, your_ssh_user, and your_ssh_password with your server's IP address and SSH credentials.


Usage
Clone this repository or download the Ansible playbook file.

Modify the playbook file (deploy_zabbix.yml) if necessary, especially the following variables in the vars section:

mariadb_zabbix_password: Set your root MySQL password.
zabbix_database_password: Set your Zabbix database password.


Run the Ansible playbook using the following command:


ansible-playbook -i inventory.ini deploy_zabbix.yml



or



ansible-playbook deploy_zabbix.yml
