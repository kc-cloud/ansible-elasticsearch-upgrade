# ansible-elasticsearch-upgrade

It provides a role for full-cluster and rolling upgrade of elasticsearch safely. This role is a wrapper around a role supplied by Elastic.co

## Prerequisite
* elasticsearch role developed by  Elastic.co (https://github.com/elastic/ansible-elasticsearch)

## Tested platforms:
Tested with python 2.7 in the following platforms
* Ubuntu 14.04
* Ubuntu 16.04

## Roles
* elasticsearch (https://github.com/elastic/ansible-elasticsearch.git)
* elasticsearch_upgrade

## Usage: 
   * download this repository
   * _cd ansible-elasticsearch-upgrade_   
   * download elasticsearch role from https://github.com/elastic/ansible-elasticsearch.git and place under _ansible-elasticsearch-upgrade/roles/elasticsearch_ folder
   * modify files under _ansible-elasticsearch-upgrade/inventory/aws/_ folder based on your environment
   * modify playbooks under _ansible-elasticsearch-upgrade/playbooks/_ for your required version to install/upgrade
   * execute _ansible-playbook -i inventory/aws <playbook yml file>_
      - _elasticsearch-install.yml_ for installing elasticsearch in the cluster
	  - _elasticsearch-full-upgrade-and-restart.yml_ for full-cluster upgrade and restart
	  - _elasticsearch-rolling-upgrade-and-restart.yml_ for rolling upgrade and restart
