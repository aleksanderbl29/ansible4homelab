# Preparation for first deployment

Before mindlessly deploying this playbook with the entire homelab there is a list of things that needs to be done first:

## Home Assistant

- [ ] Create secrets.yaml file in `./secrets/` for all corresponding secrets in the [Home Assistant config repo](https://github.com/aleksanderbl29/homeassistant-config)

## Github Actions

- [ ] Create github_actions_secret.yml in `./secrets/` with a access token that has permisison for the repo you want the runner to connect to

## Slack

- [ ] Insert slack webhook token in `./secrets/slack_code.yml` for Slack notifications to work. If needed, change the message and channel info
