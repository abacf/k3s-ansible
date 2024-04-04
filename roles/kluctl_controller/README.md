# Installs kluctl-controller on the cluster

This role installs kluctl-controller on the cluster. It downloads the kluctl binary from the official repository and installs it in the `/usr/local/bin` directory.

## Variables

The role does not require any variables.

## Example Playbook

```yaml
- hosts: servers
  roles:
    - kluctl_controller
```

## License

MIT

## Author Information

Nicolas `signed-log` FORMICHELLA - Florian `minzords` Blanchet
