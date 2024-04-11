# k3s server role

This role installs k3s as a server.

It depends on the `k3s_prepare` role to prepare the host for k3s installation.

## Variables

The role is extracted from the group name.

- If the group name is `server`, the role will install k3s as a server.

---

- It also expects `k3s_server_env`
  - This is to allow for side-by-side installation of multiple k3s servers.

```yaml
k3s_server_env: staging
```

Default being `staging`.

This is for each server to store the node key on the deployment host.

---

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
    - k3s_server
```

## Author Information

Nicolas `signed-log` FORMICHELLA - Florian `minzords` Blanchet
