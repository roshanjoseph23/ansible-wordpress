# Wordpress using Ansible

A wordpress website is created on AWS Amazon Linux EC2 and Ubuntu EC2 using Ansible

# Features

 - ansible-role
 - ansible-prompts
 - AWS
 - wordpress
 - MySQL
 - LAMP

# Prerequisites

 - One Amazon linux EC2 and an Ubuntu EC2 on AWS
 - A key pair for accessing the EC2
 - Enable `roles_path` in `/etc/ansible/ansible.cfg`
 - Wordpress download URL

## Ansible-galaxy

Ansible role is created using  `ansible-galaxy` 

    ansible-galaxy init lamp

## Wordpress create

 1. Add the server IPs in the inventory file
 2. `ansible-playbook -i inventory.txt wordpress.yml` is used to initiate the wordpress creation
 3. You can enable `inventory`path in `/etc/ansible/ansible.cfg`
     This will not require to mention the inventory file in the command line.
     `  ansible-playbook wordpress.yml`
 4. Ansible will ask for input details such as Wordpress download **URL**, **MySQL root password** to set, Wordpress **database name**, Wordpress **user name**.

## Ouput

A wordpress website configured using LAMP
