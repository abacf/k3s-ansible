# Playbooks Ansible et rôles pour k3s

Ce dépôt contient des playbooks et des rôles Ansible pour installer et configurer un cluster k3s. Cela installera également le contrôleur kluctl, un outil pour gérer les ressources Kubernetes de manière GitOps.

## Prérequis

- Ansible 2.9 ou ultérieur
- Python 3.8 ou ultérieur
- Un ensemble d'hôtes cibles exécutant Ubuntu 18.04 ou ultérieur
  . Les hôtes cibles doivent avoir un accès SSH par clé et `sudo` sans mot de passe pour l'utilisateur exécutant les playbooks Ansible.

## Utilisation

Copiez le fichier `inventory.sample.yaml` en `inventory.yml` et mettez à jour les adresses IP de vos hôtes cibles.

### Groupes d'inventaire

Les hôtes cibles sont regroupés en deux groupes d'inventaire:

- `servers`: Les hôtes qui seront les serveurs du cluster k3s
- `agents`: Les hôtes qui seront les agents du cluster k3s

Exécutez le playbook `k3s.yaml` pour installer et configurer le cluster k3s avec Kluctl:

```sh
ansible-playbook k3s.yaml
```

## Licence

Ce projet est sous licence MIT