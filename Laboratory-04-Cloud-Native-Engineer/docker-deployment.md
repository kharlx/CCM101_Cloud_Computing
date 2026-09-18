# Docker CLI Deployment & Lifecycle Guide

## Executed Commands and Explanations

* `docker --version`: Checks the currently installed version of the Docker Engine.
* `docker info`: Displays system-wide information regarding container counts, images, and configuration status.
* `docker pull nginx`: Downloads the official Nginx container image from Docker Hub to the local host environment.
* `docker run -d -p 8080:80 --name my-nginx nginx`: Starts an Nginx container in detached mode (`-d`), binding host port 8080 to container port 80 (`-p 8080:80`).
* `curl http://localhost:8080`: Sends a HTTP request to local port 8080 to verify that the containerized Nginx server is actively responding.
* `docker ps`: Lists all actively running Docker containers.
* `docker stop my-nginx`: Gracefully halts execution of the running `my-nginx` container.
* `docker ps -a`: Lists all containers on the host, including those currently stopped or exited.
* `docker rm my-nginx`: Permanently removes the stopped container instance from the host system.