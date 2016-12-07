# Ansible role: jenkins
Installs and configures jenkins.

## Requirements
None.

## Role Variables
|Key|Type|Description|Default|
|:--|:---|:----------|:------|
|jenkins_user|String||jenkins|
|jenkins_port|Integer||8081|
|jenkins_home|String||/var/lib/{{ jenkins_user }}|
|jenkins_jar_location|String||/opt/jenkins-cli.jar|
|jenkins_server_url|String||http://localhost:{{ jenkins_port }}|
|jenkins_default_plugins|Array||- git|

## Dependencies
+ [java](https://github.com/shomatan/ansible-java.git)

## Example playbook

```yaml
- hosts: all
  roles:
    - { role: jenkins }
```
