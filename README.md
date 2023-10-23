# Security Patching Task using DynamicInventory plugin with Ansible Roles

## Overview

This Ansible project includes a role designed to automate the process of applying security patches to a fleet of Linux servers. It simplifies the task of keeping your servers up-to-date and secure by using the package manager for the respective Linux distribution to update system packages.

## Prerequisites

Before using this Ansible role, ensure that you have the following prerequisites in place:

1. Ansible installed on your control node.

2. SSH access to the target servers with the necessary permissions.

3. Correctly configured AWS Dynamic Inventory.

4. AWS credentials or appropriate IAM roles for accessing EC2 instances.

## Role Structure

The project follows a role structure with the following key directories and files:

- `roles/`
  - `SecurityPatching/`
    - `tasks/`: Contains Security patch tasks defined under main.yaml for the role.
    - `files/`: Contains encrypted SSH pem file to authenticate SSH hosts
    - `vars/`: Contains SSH connection variables.
    - `DynamicInventory/`: Contains AWS dynamic inventory file.

## Usage

1. Clone or download this Ansible project to your control node.

2. Define the target servers or groups in your inventory file (`DynamicInventory`) where you want to apply security patches.

3. Include the `SecurityPatching` role in your playbook by adding roles:rolename. You can customize the role by modifying the role's variables or the playbook itself.

