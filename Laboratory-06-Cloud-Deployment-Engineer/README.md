# Laboratory 06: The Cloud Deployment Engineer

## Mission Overview
Transitioning from manual single-container deployments to Infrastructure as Code (IaC) by deploying a multi-tier private cloud storage solution (Nextcloud and MariaDB) using Docker Compose[cite: 1, 2].

## Objectives
* Explain multi-tier application architectures[cite: 1, 2].
* Understand and write `docker-compose.yml` configuration files using text editors like `nano`[cite: 1, 2].
* Deploy, verify, and teardown multi-container applications using Docker Compose[cite: 1, 2].
* Document Infrastructure as Code (IaC) principles clearly in Markdown[cite: 1, 2].

## Commands Executed
* `mkdir nextcloud-deployment && cd nextcloud-deployment` - Create and enter the project directory[cite: 1, 2].
* `nano docker-compose.yml` - Create and edit the YAML configuration blueprint[cite: 1, 2].
* `docker-compose up -d` - Build, network, and start the multi-container stack in the background[cite: 1, 2].
* `docker-compose ps` - Verify that both the Nextcloud and MariaDB containers are running (`Up`)[cite: 1, 2].
* `docker-compose down` - Gracefully stop and remove the container stack and network[cite: 1, 2].

## Skills Learned
* Infrastructure as Code (IaC) implementation with Docker Compose[cite: 1, 2].
* Multi-tier architecture design (Web Tier + Database Tier separation)[cite: 1, 2].
* Container networking and secure environment variable configuration[cite: 1, 2].
* Technical Markdown documentation and GitHub portfolio management[cite: 1, 2].