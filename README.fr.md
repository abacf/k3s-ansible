# Playbooks Ansible et rôles pour k3s

Ce dépôt contient des rôles Ansible pour installer et configurer un cluster k3s.

Ainsi que le rôle pour installer `kluctl` GitOps.

## Prérequis

- Ansible 2.9 ou ultérieur
- Python 3.8 ou ultérieur
- Un ensemble d'hôtes cibles exécutant Ubuntu 18.04 ou ultérieur
  - Les hôtes cibles doivent avoir un accès SSH par clé
  - `sudo` sans mot de passe pour l'utilisateur exécutant les playbooks Ansible.

### Groupes d'inventaire

Les hôtes cibles sont regroupés en deux groupes d'inventaire:

- `servers`: Les hôtes qui seront les serveurs du cluster k3s
- `agents`: Les hôtes qui seront les agents du cluster k3s

## Utilisation

- Copiez le fichier `inventory.sample.yaml` en `inventory.yml`

- Mettez à jour les adresses IP de vos hôtes cibles.

- Exécutez le playbook `k3s.yaml` pour installer le cluster k3s et Kluctl:

```sh
ansible-playbook k3s.yaml
```

## Licence

Ce projet est sous licence MIT
