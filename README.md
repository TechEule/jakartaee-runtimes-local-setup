# TechEule - Ansible local setup for Jakarta EE /Java EE runtimes

## Requirements

* OS: MacOS x, Linux, UNIX
* Software: JDK and Ansible

## Usage

### Install all runtimes at once

```shell
ansible-playbook -i ./inventories/localhost main.yml 
```

### Install only runtime Open Liberty

```shell
ansible-playbook -i ./inventories/localhost main.yml --tags 'openliberty'  
```

### Install only runtime Payara

```shell
ansible-playbook -i ./inventories/localhost main.yml --tags 'payara'  
```

### Install only runtime Wildfly

```shell
ansible-playbook -i ./inventories/localhost main.yml --tags 'wildfly'  
```
