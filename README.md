# Mini Project 1 — Automated Server Environment Setup

## Overview
This project provisions a two-server environment using Vagrant and VirtualBox.
A web server and database server are automatically configured using Infrastructure as Code principles.

## Infrastructure
| Server | IP Address | Role | OS |
|---|---|---|---|
| webserver | 192.168.56.20 | Web Server | Ubuntu 22.04 |
| dbserver | 192.168.56.21 | Database Server | Ubuntu 22.04 |

## Technologies Used
- Vagrant — Infrastructure provisioning
- VirtualBox — Virtualisation
- Bash — Automation scripting
- YAML — Infrastructure documentation
- Git & GitHub — Version control

## Features
- Automated two-VM environment with a single `vagrant up` command
- Nginx installed and enabled automatically on the webserver via Vagrant provisioning
- Bash script to display server information and log output
- Infrastructure documented in YAML format
- Full Git history with meaningful commits

## Prerequisites
- Vagrant installed
- VirtualBox installed
- Git installed

## How To Run
Clone the repository:
\```bash
git clone git@github.com:Youngprilo/mini-project-1.git
cd mini-project-1
\```

Spin up the environment:
\```bash
vagrant up
\```

SSH into the webserver:
\```bash
vagrant ssh webserver
\```

Run the server info script:
\```bash
chmod +x server-info.sh
./server-info.sh production
\```

Check the provision log:
\```bash
cat /home/vagrant/provision.log
\```

## Project Structure
\```
mini-project-1/
├── Vagrantfile          # Defines the VM environment
├── infrastructure.yaml  # Documents the infrastructure
├── server-info.sh       # Server information script
└── README.md            # Project documentation
\```

## Author
Micah — DevOps Engineer in Training
