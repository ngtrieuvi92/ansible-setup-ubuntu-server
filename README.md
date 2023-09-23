# Initial Server Setup on Ubuntu 22.04 LST
Explain more about this package ( Vietnamese version): [https://vinguyen.blog/cac-viec-nen-lam-sau-khi-setup-server-ubuntu-linux-moi-tren-cloud/](https://vinguyen.blog/cac-viec-nen-lam-sau-khi-setup-server-ubuntu-linux-moi-tren-cloud/)

## Settings
- `target_user`: the name of the new user
- `ssh_public_key_paths`: array of public key add to authorized_keys
- `sys_packages`: array with list of packages that should be installed.


## Running this Playbook

#### Default variables
```yml
necessary_packages: ['curl', 'vim', 'git', 'ufw', 'htop', 'iotop', 'apt-transport-https', 'acl', 'python3-paramiko']
swap_vars:
  size: 1G
  swappiness: 60
```

Quick Steps:

### 1. Obtain the playbook
```shell
ansible-galaxy install ngtrieuvi92.setup_ubuntu_sever
```

### 2. Delare host in host.ini file

```shell
nano host.ini
```
### 3. Run the Playbook

```shell
ansible-playbook -i hosts.ini setup-new-instance-playbook.yml
```