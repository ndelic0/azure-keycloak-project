# Azure Keycloak Deployment with Terraform and Ansible

This repository contains the infrastructure and application deployment setup for deploying Keycloak on Azure. It uses **Terraform** to create the infrastructure resources and **Ansible** for provisioning the Keycloak server and related components, including the Docker setup.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Directory Structure](#directory-structure)
- [Usage](#usage)
  - [Deploying the Infrastructure](#deploying-the-infrastructure)
  - [Deploying the Application](#deploying-the-application)
- [GitHub Actions](#github-actions)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project automates the process of deploying Keycloak on Azure using the following steps:

1. **Provisioning infrastructure with Terraform**:
   - A virtual network, subnet, and public IP are created on Azure.
   - An Azure virtual machine is provisioned with an SSH key for access.

2. **Setting up Keycloak with Ansible**:
   - Docker is installed on the VM.
   - Docker Compose is used to deploy Keycloak and a PostgreSQL database.
   - Keycloak is configured with default credentials.

## Prerequisites

Before you can deploy the infrastructure and application, you’ll need to set up the following:

1. **Terraform** - Ensure you have Terraform installed. You can download it from [Terraform's website](https://www.terraform.io/downloads.html).
2. **Ansible** - Ansible is required to manage the configuration of the server. Install it via pip:
   ```bash
   pip install ansible
