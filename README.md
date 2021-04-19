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

## Aliases in shell

```sh
export BOC_TOOLS="${HOME}/tools/boc-tools"


alias wildfly-reinstall='(cd ${BOC_TOOLS} && ansible-playbook main.yml -i inventories/localhost --tags 'wildfly' > /dev/null 2>&1 || echo "error")'

alias keycloak-reinstall='(cd ${BOC_TOOLS}  && ansible-playbook main.yml -i inventories/localhost --tags 'keycloak' > /dev/null 2>&1 || echo "error")'

alias tomee-reinstall='(cd ${BOC_TOOLS}  && ansible-playbook main.yml -i inventories/localhost --tags 'tomee' > /dev/null 2>&1 || echo "error")'

alias openliberty-reinstall='(cd ${BOC_TOOLS}  && ansible-playbook main.yml -i inventories/localhost --tags 'openliberty' > /dev/null 2>&1 || echo "error")'

alias payara-reinstall='(cd ${BOC_TOOLS}  && ansible-playbook main.yml -i inventories/localhost --tags 'payara' > /dev/null 2>&1 || echo "error")'

alias jee-rt-reinstall='(cd ${BOC_TOOLS}  && ansible-playbook main.yml -i inventories/localhost  > /dev/null 2>&1 || echo "error")'

alias openliberty-start='${LIBERTY_HOME}/bin/server run'

alias wildfly-start='${WILDFLY_HOME}/bin/standalone.sh '

alias tomee-start='${TOMEE_HOME}/bin/catalina.sh run'

alias payara-start='${PAYARA_HOME}/glassfish/bin/startserv'
```
