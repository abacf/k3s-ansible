# Ansible playbooks and roles for k3s and kluctl

[Français](README.fr.md)

This repository contains Ansible playbooks to install and configure a k3s cluster.

This will also install the kluctl GitOps controller

## Requirements

- Ansible 2.9 or later
- Python 3.8 or later
- A set of target hosts running Ubuntu 18.04 or later
  . The target hosts must have passwordless SSH
  - password-less `sudo` access enabled for the user running the Ansible playbooks.

### Inventory groups

The target hosts are grouped into two inventory groups:

- `servers`: The hosts that will be the servers of the k3s cluster
- `agents`: The hosts that will be the agents of the k3s cluster

## Usage

- Copy the `inventory.sample.yaml` file to `inventory.yml`

- Update the IP addresses of your target hosts.

- Run the `k3s.yaml` playbook to install the k3s cluster along with Kluctl

```sh
ansible-playbook k3s.yaml
```

## License

This project is licensed under the MIT License
