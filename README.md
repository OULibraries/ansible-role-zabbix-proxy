OU Libraries Zabbix
=========

Rudimentary Zabbix zerver role for CentOS 7.
See the [Zabbix 3.0 documentation](https://www.zabbix.com/documentation/3.0/manual).

Requirements
------------

This role requires:

- [OULibraries.centos7](https://github.com/OULibraries/ansible-role-centos7)
- [OULibraries.mariadb](https://github.com/OULibraries/ansible-role-mariadb)
- [OULibraries.zabbixagent](https://github.com/OULibraries/ansible-role-zabbix-agent)


Role Variables
--------------

The following variables are defined:

```
httpd_dn_prefix: proxy
httpd_dn_suffix: vagrant.dev

# DB admin user for creating zabbix db 
mariadb_host: localhost
mariadb_port: 3306
mariadb_root_user: root
mariadb_root_pass: root

# Zabbix DB and Credentials
zabbix_db: zabbix
zabbix_db_user: zabbix
zabbix_db_pass: zabbix

# Zabbix Server IP and name proxy is defined as on server - must match

zabbix_server_ip: 10.255.255.10
zabbix_proxy_name: proxy

#Proxy TLS Encryption Information - Must also be defined on server
zabbix_psk_ident: proxy
zabbix_psk: 1f87b595725ac58dd977beef14b97461a7c1045b9a1c963065002c5473    194952

```
