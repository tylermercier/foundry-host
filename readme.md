Based playbook on https://gitlab.com/davefp/foundry-vtt-config

# Foundry VTT Server Configuration

This repo contains an Ansible playbook for configuring a server to run the Foundry VTT software.

Currently, the playbook will:

* Install dependencies (nodejs, caddy, unzip)
* Create a foundry user/group
* Extract the Foundry app onto the remote server
* Set up a data directory for Foundry to use
* Configure caddy to reverse proxy the app
* Set up a systemd unit to run the app

# Usage instructions

## Assumptions

* You already have a VPS running and DNS records pointing your desired domain at it.
* You have a valid SSH key for your root user configured in your SSH agent.
* You have Ansible installed and are reasonably familiar with it. `brew install ansible`
* You have a valid, licensed copy of the Foundry VTT server software in a zip file on your local machine

## Steps

Create a copy of the example variables file `cp variables.yml.example variables.yml` and change the domain name to the correct value.

Make sure the Foundry zip file is in the root of this project and called `foundryvtt.zip`.

Run the playbook against your server, e.g. `ansible-playbook playbook.yml -i vtt.vidja.ca,` (Note the comma after the domain, this tells ansible it's an address and not an inventory file).

## Restarting foundry

From the server, run `sudo systemctl restart foundryvtt.service`

## Updating foundry

Download the latest version


Rename the file to `foundryvtt.zip` and place it in the repo
Run `ansible-playbook playbook.yml -i vtt.vidja.ca,`