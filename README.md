# ansible-zabbix-4.0-mysql

This is a basic ansible playbook (well, set of playbooks) for
setting automatically setting up a mariadb-backed Zabbix 4.0 server
including all necessary dependencies and selinux setup on CentOS 7

This setup is intended as a single-node install.

Edit variables within vars/ directory to your liking.
Edit inventory to work to your specifications

TO-DO:
 - Convert each sub-playbook into a separate role
 - Migrate passwords to ansible-vault
 - Add zabbix agent role
 - Merge selinux modules

