# Ansible Scripts Repository
This repository contains playbooks and all necessary scripts for creating and managing AWS Resources using Ansible

## Prerequisites
To use the playbooks in this repository, Ansible must be installed on your local machine.

Note: As of writing, the version of Ansible being used is 2.2.0.0.
To install using apt-get:
```
sudo apt-get install ansible
```
To install using yum:
```
sudo yum install ansible
```
To install using pip:
```
sudo pip install ansible
```
It is preferred to install using pip since pip repositories have more Ansible versions available.

## Basic Usage
Ansible runs only the playbooks stored in the ansible_scripts directory. All other scripts and files are called by the playbook.
Running an ansible playbook is done via:
```
ansible-playbook -i [env] [-e variable=value] ansible_scripts/playbook.yaml
```
Where:
* [env] is a directory pertaining to a specific environment. Such environment directories make use of an inventory script for AWS - See [Ansible Dynamic Inventories](http://docs.ansible.com/ansible/intro_dynamic_inventory.html)
* [-e] are extra variables used in the playbook, but are not preset in the environment directory group vars.
