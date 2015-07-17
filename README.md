### Overview:
This is an ansible playbook for deploying Galera-MariaDB on three CentOS 7 servers.

### Prerequisites:
3x CentOS 7 servers
1x staging server or PC running Ansible 1.9.2 

### Deployment:
Edit your local /etc/hosts file and add your 2 CentOS server IPs and hostnames.

```
192.168.0.1 galera1
192.168.0.2 galera2
192.168.0.3 galera3
```

Next please add server IPs to the variables located in /group_vars/all

```
galera1ip: "192.168.0.1"
galera2ip: "192.168.0.2"
galera3ip: "192.168.0.3"
```

You're now ready to run the playbook!

```
ansible-playbook -i hosts site.yml 
```
