# Ansible Playbook for PostgreSQL Cluster

PostgreSQL Cluster (Pgpool-II + PostgreSQL SR/HS)

## How to use

List all currently targeted hosts.

```Shell
ansible all --list-hosts -i pg-cluster/inventory/hosts.yml
```

Runs Ansible playbooks.

```Shell
ansible-playbook -i pg-cluster/inventory/hosts.yml pg-cluster/site.yml
```

## Requirements

In order to execute normally, the following OS package is required.

### PostgreSQL Server

These package is needed for installing pgpool-recovery

* gcc (2.9 or later)
* make

### Pgpool-II Server

These package is needed for using watchdog

* iputils
* iproute or net-tools

NOTICE: net-tools is deprecated. iproute is recommended.
