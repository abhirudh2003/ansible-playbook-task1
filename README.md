# Ansible for Configuration Management – Docker Automation

## 1. Project Overview

This project uses Ansible to automate Docker installation and container deployment on a remote AWS Ubuntu server using ssh.

## 2. Project Objectives

- Install Docker automatically using Ansible.
- Pull a Docker image from a container registry.
- Run a Docker container on the managed server.
- Automate server configuration and deployment.

## 3. Technologies Used

- Ansible
- Docker
- Ubuntu
- AWS EC2 ( two instances )
- YAML
- GitHub

## 4. Project Architecture

AWS instance 1 (Control Node)
↓ SSH Connection
AWS instance 2 (Managed Node)
↓
Ansible Playbook
↓
Docker Installation
↓
Docker Image Pull
↓
Docker Container Running

## 5. Project Files

- `ansible-docker-inventory.ini` – Managed node configuration.
- `ansible-docker-playbook.yml` – Main automation playbook.

## 6. Execution

Run the following command from the project directory:

```bash
ansible-playbook -i ansible-inventory.ini ansible-docker-playbook.yml
```

## 7. Verification

Verify Docker installation:

```bash
docker --version
```

Check running containers:

```bash
docker ps
```

## 8. Expected Result

Ansible successfully installs Docker, pulls the specified image and starts the container automatically on the managed Linux server.

## 9. Conclusion

This project demonstrates how Ansible can simplify configuration management and automate Docker deployment on remote servers.
