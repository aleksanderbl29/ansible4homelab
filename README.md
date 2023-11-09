# ansible4homelab

Ansible config for my homelab

## To do

I want to implement these features:

### Larger and structural features

- [ ] Automatic testing of the playbook with molecule in Github Actions
- [ ] Ability to use same playbook for continuous deployment (CD) triggered from updates to my [homelab](https://github.com/aleksanderbl29/homelab) repository here on Github

### Move manual deployment to ansible

- [ ] [Configuration for Uptime Kuma](https://github.com/aleksanderbl29/ansible4homelab/issues/3)

## Steps

This playbook currently goes through these steps to deploy my entire homelab config

```mermaid
---
title: Initial deployment
---
flowchart TD
  main("main.yml")
  main_pre_tasks("Update apt cache")
  main_tasks("Setup Docker
  Clone Git Repos")
  setup_docker("Ensure Docker is setup")
  clone_repos("Clone homelab repository")
  clone_ha_repo("Clone repository with config for Home Assistant")

  main --> main_pre_tasks
  main_pre_tasks --> main_tasks

  main_tasks --> setup_docker
  main_tasks --> clone_repos  --> |If hostname includes HA| clone_ha_repo
``````

## Preparation

When running this playbook [here](./preparation.md) is a list of things that needs to be done first, e.g. collection tokens and creating secrets

## Credits

I have drawn a lot of inspiration from Jeff Geerling's work with ansible. I also use his book to learn ansible while moving my manual deployment to ansible.
