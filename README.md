# Ansible playbooks and roles for k3s and kluctl

[Français](README.fr.md)

This repository contains Ansible playbooks and roles to install and configure a k3s cluster. This will also install kluctl controller, a tool for managing kubernetes ressources in a GitOps way.

## Requirements

- Ansible 2.9 or later
- Python 3.8 or later
- A set of target hosts running Ubuntu 18.04 or later
  . The target hosts must have passwordless SSH and `sudo` access enabled for the user running the Ansible playbooks.

## Usage

Copy the `inventory.sample.yaml` file to `inventory.yml` and update the IP addresses of your target hosts.

Run the `k3s.yaml` playbook to install and configure the k3s cluster along with Kluctl:

```sh
ansible-playbook k3s.yaml
```

## License

This project is licensed under the MIT License