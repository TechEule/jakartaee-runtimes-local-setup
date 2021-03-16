# TechEule - Ansible local setup for Jakarta EE (Java EE) runtimes (Servers)

## Supported Runtimes

* [Open Liberty](https://openliberty.io/)
* [Payara](https://www.payara.fish/)
* [TomEE](http://tomee.apache.org/)
* [Wildfly](https://www.wildfly.org/)
* [Keycloak](https://www.keycloak.org/)

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

### Install only runtime TomEE

```shell
ansible-playbook -i inventories/localhost main.yml --tags 'tomee'
```

### Install only runtime Keycloak

```shell
ansible-playbook -i ./inventories/localhost main.yml --tags 'keycloak'  
```
