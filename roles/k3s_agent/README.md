# k3s server role

This role installs k3s as a server.

It depends on the `k3s_prepare` role to prepare the host for k3s installation.

## Variables

The role is extracted from the group name.

- If the group name is `agent`, the role will :
  - install k3s as an agent
  - and join to the cluster.

**Only one server is currently supported if you use the `k3s_agent` role.**

The Inventory file should look like this:

```yaml
k3s_cluster:
  children:
    server:
      hosts:
        192.16.35.11:
    agent:
      hosts:
        192.16.35.12:
        192.16.35.13:
```

## Example Playbook

```yaml
- hosts: k3s_cluster
  roles:
    - k3s_agent
```

## Author Information

Nicolas `signed-log` FORMICHELLA - Florian `minzords` Blanchet
