# Ansible-Bind-DNS-Cluster
DNS Cluster with Ansbile and using Bind9

## Getting Started
If you want have two Bind9 DNS Server (master/slave) you can use this playbook for deploying servers.

### Installing
Before Installing, You must modify variables in group_vars/all
```
ansible-playbook main.yml -i hosts.yml
```
### Add Zone to server
If you want add a zone with primary and secondary nameserver to cluster you can use this:
```
ansible-playbook add_zone.yml -i hosts --extra-vars="bind_config_master_zones=example.com"
```
