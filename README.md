tendrl-ansible
============

Ansible playbook for Tendrl!

Clone me:

```bash
git clone https://github.com/Tendrl/tendrl-ansible.git
```

## What does it do?

General support for:

* Tendrl Central Store
* Tendrl API Server
* Tendrl Agents


## Getting Started

The [infrastructure](infrastructure) file serves as an example inventory. Look at it, change the hostnames to fit your deployment and then execute

```
ansible-playbook -i infrastructure site.yml
```

The Host in the `tendrl-servers` group will get the Tendrl Central Store (Etcd) and the Tendrl API Server installed and hosts in the `storage-servers` group will get the Tendrl Agent installed.

**Note** Currently there is only support for a single server in the tendrl-servers group!

## VirtualBox Support

If you would like to bring up a small testbed with Tendrl and two storage nodes:

git clone https://github.com/Tendrl/tendrl-ansible.git

cd tendrl-ansible/

$ ansible-galaxy install -p roles/ geerlingguy.apache

$ ansible-galaxy install -p roles/ geerlingguy.ntp

vagrant up --no-provision

vagrant provision

browse to http://localhost:8080
