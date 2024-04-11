# k3s prepare role

This role prepares the host for k3s installation.

- Checks if k3s is already installed and if it is, it will not install it again.
- Fetches the k3s installation script.
- It also checks if the host is a server or an agent

## Variables

Role is extracted from the group name.

- If the group name is `server`, the role will prepare k3s as a server.
- If the group name is `agent`, the role will prepare k3s as an agent.

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
    - k3s_prepare
```

## License

MIT

## Author Information

Nicolas `signed-log` FORMICHELLA - Florian `minzords` Blanchet
