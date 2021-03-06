# Electronic Payment Integration Platform - Environment Automation

This repo contains the ansible scripts + docker-compose file to install/update the eFiling App Tier environments + run docker container.

## What is this repository for

* Installs and updates E-Payment (EPIP) environments

## Environments

Since this is only the playbooks projects, please find the available environments into the epip-ansible-<owner/coutry> repositories

## How to set up

Make sure you have Ansible 2.8.5 installed.

``` bash
sudo apt-get update && sudo apt-get -y upgrade
sudo apt-get install python-pip
sudo pip install 'ansible==2.8.5'
```

## Install - Prefered installation order

### 1. Installs Docker and Containers

ansible-playbook -i environments/\<env-folder>/\<inventory-file> docker.yml --ask-vault-pass

### 2. Deploy - New Releases

ansible-playbook -i environments/\<env-folder>/\<inventory-file> docker.yml --tag deploy --ask-vault-pass
