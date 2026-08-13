# Cloud Infrastructure Components Analysis

## 1. Compute Resources
* **Purpose:** Compute resources handle all the heavy lifting, executing system processes, processing data, and running application code through the server's CPU and RAM.
* **Importance in Cloud Computing:** In cloud architecture, compute power lets us spin up or scale virtual machines on demand whenever user traffic spikes, eliminating the need to physically upgrade hardware.
* **Linux Environment Context:** Based on my system audit using `lscpu` and `free -h`, our KillerCoda VM runs on 1 vCPU core (Intel Xeon E312xx @ 2.0GHz) paired with 1.9 GiB of total RAM.

---

## 2. Storage Resources
* **Purpose:** Storage keeps all essential system files, operating system binaries, databases, and project assets safe and intact even when the instance restarts.
* **Importance in Cloud Computing:** It provides reliable data persistence, allowing us to attach, detach, take snapshots, or expand virtual storage drives dynamically without affecting the main server instance.
* **Linux Environment Context:** Running `df -h` showed that our environment uses a primary root partition (`/dev/vda1`) with a 19 GiB total capacity (currently at 30% usage) alongside an 881 MiB `/boot` partition.

---

## 3. Networking Resources
* **Purpose:** Networking establishes communication paths, manages IP routing, and controls data transfers between virtual servers, local subnets, and external web users.
* **Importance in Cloud Computing:** It builds the foundation for security and isolation using Virtual Private Clouds (VPCs), subnets, routing tables, and firewalls to keep cloud workloads protected.
* **Linux Environment Context:** Checking `ip a` revealed our primary network adapter `enp1s0` configured with a private IP address of `172.30.1.2/24`, as well as an active `docker0` bridge network interface.

---

## 4. Operating System (OS)
* **Purpose:** The OS serves as the main bridge between virtualized server hardware and higher-level software applications or user tools.
* **Importance in Cloud Computing:** It gives developers a standardized, secure environment loaded with necessary dependencies, system libraries, and package managers for deploying apps smoothly.
* **Linux Environment Context:** Using `hostnamectl`, I confirmed that our cloud instance is running Ubuntu 24.04.4 LTS on top of Linux Kernel 6.8.0-136-generic.