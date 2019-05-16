# ansible-zabbix-mysql

This is a basic ansible playbook for automatically setting up a mariadb-backed
Zabbix server including all necessary dependencies and selinux setup on CentOS 7.

Basic setup was indended for a single-node deploy, but can be deployed to multiple nodes.
To achieve multi-node setup, edit inventory:
 - Zabbix server stack will be installed on the "zabbixserver" host group node.
 - Mariadb dabatabse will be installed on the "dbserver" host group node.
 
and variables:
 - mariadbhostip denotes the IP of the DB server node for connection purposes.

Edit variables within vars/ directory to your liking, they override defaults set up in
zabbix roles.
Edit inventory to work to your specifications. 

New: The "zbxvers" variable allows you to set the Zabbix release version for install.

Note: only versions 4.0-4.2 have been tested so far. YMMV with older/newer releases.

Start setup by running:
    ansible-playbook install.yml

TO-DO:
 - Migrate passwords to ansible-vault
 - Add zabbix agent role
 - Merge selinux modules

