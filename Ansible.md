***

## Ansible is a tool that can automatic execute shell commands and scripts on several machines at a time.

***

## Ansible :

- #### Python-based
- #### Agentless
- ##### use SSH
- #### use Push model delivery

***

## Ansible directory is /etc/ansible

 - ### 'hosts' file contain groups of machines by ip/domain

```sh
[webservers]
alpha.example.org
beta.example.org
192.168.1.100
192.168.1.110
```

- ### 'ansible.cfg' contain ansible config

***

## Create playbook

- #### Playbook are automation blueprints, in YAML format.
- #### Play is ordered list of tasks that maps to managed nodes in hosts
- #### Task is a list of modules that define operations ansible will do
- #### Module is a unit of code that Ansible runs, modules grouped in collections with a FQCN.


