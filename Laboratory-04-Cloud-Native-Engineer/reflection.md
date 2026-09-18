# Mission Reflection

The boot time and setup process of a Docker container are significantly faster than those of a traditional Virtual Machine. While a VM requires setting up hypervisors, installing full guest operating systems, and waiting minutes for boot cycles, a Docker container shares the host system kernel and spins up within seconds.

Port mapping using `-p 8080:80` is necessary because containers run in isolated network namespaces. Port mapping exposes the internal container network port (80) to an accessible port on the host machine (8080), allowing external or local network traffic to reach the application running inside.

When executing `docker rm`, the container instance and its isolated read-write file layer are permanently deleted. Any ephemeral data saved inside the container that was not written to a persistent volume or bind mount is lost.

Containerization transforms collaboration between software developers and IT operations by establishing consistency across environments. Developers can package application code alongside dependencies into standardized images, ensuring that code running in local development operates identically in production environments.

My GitHub Cloud Computing Portfolio is evolving into a structured technical repository, demonstrating practical proficiency across Linux administration, multi-cloud platforms, and cloud-native containerization.