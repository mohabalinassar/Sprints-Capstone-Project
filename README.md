# Sprints-Capstone-Project
# Jenkins Setup Guide

This guide provides step-by-step instructions to set up Jenkins using Terraform and Ansible. It covers the installation process, connecting to Jenkins, creating user accounts, configuring credentials, and setting up a GitHub webhook for automation.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- Terraform installed
- Ansible installed
- AWS account and AWS CLI configured
- SSH access to the target server

## Installation Steps

### Step 1: Terraform Setup

1. Run the following commands in your terminal to initialize Terraform and apply the configuration:

   ```shell
   terraform init
   terraform plan
   terraform apply
### Step 2: Install Jenkins using Ansible
Run the following Ansible playbook commands to install Jenkins, Docker, AWS CLI, and kubectl:

```shell
ansible-playbook docker.yml -i inventory.txt
ansible-playbook Jenkins.yml -I inventory.txt
ansible-playbook awscli.yml -i inventory.txt
ansible-playbook kubectl.yml -i inventory.txt
