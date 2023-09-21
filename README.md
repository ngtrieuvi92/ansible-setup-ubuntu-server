# Initial Server Setup on Ubuntu 22.04 LST

## Settings
- `target_user`: the name of the new user
- `ssh_public_key_paths`: array of public key add to authorized_keys
- `sys_packages`: array with list of packages that should be installed.


## Running this Playbook

Quick Steps:

### 1. Obtain the playbook
```shell
git clone git@github.com:ngtrieuvi92/ansible-setup-ubuntu-server.git
cd ansible-playbooks/setup_ubuntu1804
```

### 2. Delare host in host.ini file

```shell
nano host.ini
```
### 3. Run the Playbook

```shell
ansible-playbook -i hosts.ini setup-new-instance-playbook.yml
```