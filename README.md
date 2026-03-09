# Jenkins + Ansible Pipeline

Automates nginx installation on a target server using Jenkins CI/CD and Ansible.

## Stack
- **Jenkins** — CI/CD pipeline
- **Ansible** — Configuration management
- **AWS EC2** — Ubuntu instances

## How It Works
1. Jenkins pulls code from GitHub
2. Jenkins triggers Ansible playbook
3. Ansible SSHs into target server
4. Nginx is installed and started

## Project Structure
```
jenkins_ansible/
├── Jenkinsfile   # Jenkins pipeline definition
├── inventory     # Target server details
└── playbook.yml  # Ansible tasks
```

## Requirements
- Jenkins Server with Ansible installed
- Target EC2 instance with `ansible` user configured
- SSH key-based authentication between servers
