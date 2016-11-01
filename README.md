Pi Unifi Controller
===================

This project intend to automatically deploy UniFi Controller v5 to Raspberry Pi.

Prerequisites
-------------

A Raspberry Pi provisioned with Raspbian

Usage
-----

### Initialize raspberry

 - Drop your public ssh key in ssh-keys/files/enabled
 - Run prepare.yml playbook with default pi user
 
    ansible-playbook -i inventories/hosts prepare.yml -e ansible_ssh_user=pi -e ansible_ssh_pass=raspberry

### Deploy UniFi Controller

 - Run deploy playbook with previously provisioned ansible user.
    
    ansible-playbook -i inventories/hosts deploy.yml

TODO
----

 - Disable pi user ssh authentication
 - Configure firewall
 - Configure reverse proxy 
