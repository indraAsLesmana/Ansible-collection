# Ansible Configuration Collection

This project is a collection of Ansible configurations. It contains various playbooks, roles, and inventory files to automate and manage your infrastructure.

## Installation

To install Ansible, you can use the package manager for your operating system. Below are the instructions for some common platforms:

### macOS

```bash
brew install ansible
```

### Ubuntu

```bash
sudo apt update
sudo apt install ansible
```

### CentOS

```bash
sudo yum install epel-release
sudo yum install ansible
```

## Running Ansible

To run Ansible playbooks, use the following command:

```bash
ansible-playbook -i inventory playbook.yml
```

Replace `inventory` with your inventory file and `playbook.yml` with the playbook you want to run.

### Example with Custom Directory

If your inventory and playbook files are located in custom directories, you can specify their paths directly in the command. For example:

```bash
ansible-playbook -i ~/Ansible/inventory ~/Ansible/cloudflare_argo.yml
```

In this example:
- `~/Ansible/inventory` is the path to your inventory file.
- `~/Ansible/cloudflare_argo.yml` is the path to your playbook file.

This allows you to organize your Ansible files in directories of your choice while still being able to execute them easily.

## Running Ansible on a Remote Server

To run Ansible playbooks on a remote server, you need to specify the remote server's details in your inventory file. Here is an example command:

```bash
ansible-playbook -i inventory playbook.yml -u username -k
```

- Replace `inventory` with your inventory file.
- Replace `playbook.yml` with the playbook you want to run.
- Replace `username` with the username for the remote server.
- The `-k` option will prompt you for the SSH password.

Ensure that the remote server is accessible via SSH and that the necessary permissions are configured. For more details, refer to the [Ansible documentation](https://docs.ansible.com/ansible/latest/index.html).

For more information, refer to the [Ansible documentation](https://docs.ansible.com/ansible/latest/index.html).