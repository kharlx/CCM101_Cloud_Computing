# Laboratory 04: The Cloud-Native Engineer

## Mission Overview
Transitioning from traditional virtual machine setups to containerized environments using Docker. This activity demonstrates the execution of basic Docker CLI commands, port mapping, and container lifecycle management inside a Linux environment.

## Objectives
* Differentiate between Virtual Machines and Containers.
* Access Docker within KillerCoda.
* Execute foundational Docker CLI commands.
* Deploy, manage, and terminate an Nginx web server container.
* Document technical workflows using Markdown.

## Docker Commands Executed
* `docker --version`
* `docker info`
* `docker pull nginx`
* `docker run -d -p 8080:80 --name my-nginx nginx`
* `curl http://localhost:8080`
* `docker ps`
* `docker stop my-nginx`
* `docker ps -a`
* `docker rm my-nginx`

## Skills Learned
* Container lifecycle management (pull, run, stop, remove).
* Host-to-container port mapping (`-p` flag).
* Basic CLI navigation for cloud-native tools.

## Challenges Encountered
* Ensuring the correct port mapping syntax (`host_port:container_port`) so local traffic resolves to the Nginx instance inside the container.