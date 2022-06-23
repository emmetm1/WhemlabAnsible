# WhemlabAnsible
Ansible deployment for homelab. Attempting to follow best practices as outlined here: https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html#content-organization

Only works for prometheus at the moment

# Overview
This repo holds playbooks for a multitude of tasks. This documentation will outline the function of the various playbooks by project. The hosts.ini file contains all groups and hosts for all the project listed below. Some playbooks are run on a schedule from ansible tower at https://ansible.whemhome/#/login

The user for the ansible host is AnsibleMaster.

In addition to the playbooks in the repo, I also use some roles from ansible galaxy. These roles can be found at /home/AnsibleMaster/.ansible/roles

## Updates
DebUp.yml updates all Debian based hosts and reboots them if needed. This playbook runs weekly from Tower. In the future this should be expanded to add update support for rhel machines.

update_pihole.yml updates the pihole application using a bash command. It is run daily from Tower.

## System Setup/Docker
mounts.yml can be used on any system to add the Whemfiles and Media network mounts. The playbook ensures that all require utilities are installed.

dockerinstall.yml uses geerlingguy's ansible galaxy role to install docker on rhel or deb. https://galaxy.ansible.com/geerlingguy/docker

## Temp monitoring
TempmonStatus.yml restarts the tempmon process on the pis. This playbook is run with Tower frequently. This only exists because my python for monitoring the temp sensors is garbage...

## Prometheus
The configs folder holds all the config files for prometheus and its various parts. promstackupdate.yml looks for config changes and updates the config files and restarts the containers as needed.

node_exporter.yml uses geerlingguy's ansible galaxy role to install node exporter on rhel or deb. https://galaxy.ansible.com/geerlingguy/node_exporter
