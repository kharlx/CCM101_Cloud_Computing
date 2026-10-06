# Docker Compose Technical Guide

## Understanding the YAML Configuration

### 1. What does the `services:` block do?
The `services:` block defines the individual containers that make up your multi-container application stack[cite: 1, 2]. Each service under this block acts as an independent blueprint for a container, specifying its container image, environment variables, port mappings, and networking rules[cite: 1, 2]. In our project, we defined two services: `database` and `app`[cite: 1, 2].

### 2. How did the Nextcloud app container find the database container?
The Nextcloud app container locates the database container using Docker's built-in automatic service discovery and DNS resolution[cite: 1, 2]. By setting the environment variable `MYSQL_HOST=database` (which matches the exact service name defined in our Compose file), the Nextcloud container resolved the hostname `database` directly to the MariaDB container's internal IP address on the shared Docker network[cite: 1, 2].

### 3. What is the difference between `docker run` and `docker-compose up -d`?
* **`docker run`**: Used to manually deploy a single container at a time[cite: 1, 2]. It requires long command lines with multiple manual flags (`--name`, `-p`, `-e`, `--network`), making it tedious and error-prone when managing multi-tier applications[cite: 1, 2].
* **`docker-compose up -d`**: An Infrastructure as Code (IaC) command that reads our `docker-compose.yml` file to provision, link, network, and start the entire multi-container stack simultaneously in the background (`-d`) with a single command[cite: 1, 2].