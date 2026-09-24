# Ansible Infrastructure

Ansible configuration for managing my homelab infrastructure.

## Current scope

- Raspberry Pi systems
- Linux baseline configuration
- Automation account bootstrapping

## Structure

- `inventories/production/` - Production inventory and variables
- `playbooks/` - Ansible playbooks
- `collections/requirements.yml` - Required Ansible collections

## Requirements

- ansible-core 2.21
- Required collections installed with:

  `ansible-galaxy collection install -r collections/requirements.yml`

## Usage

Test connectivity:

`ansible all -m ansible.builtin.ping`

Apply the Linux baseline:

`ansible-playbook playbooks/baseline.yml`
