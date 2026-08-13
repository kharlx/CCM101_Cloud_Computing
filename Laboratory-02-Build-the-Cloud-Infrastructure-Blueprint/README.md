# Laboratory 02: Build the Cloud Infrastructure Blueprint

## Mission Overview
The main goal of this activity was to audit a virtual Linux server on KillerCoda. By running essential system administration commands, I inspected the virtual hardware, disk storage, and network setups to build a solid cloud infrastructure blueprint and compare top cloud providers.

---

## Objectives
* Audit system details, CPU, RAM, storage, and networking on a live Linux machine.
* Map actual system specs to core cloud infrastructure pillars.
* Compare equivalent services across AWS, Microsoft Azure, and Google Cloud Platform.
* Design a clean cloud architecture diagram showing data flow from user to storage.
* Document all findings cleanly using Markdown for Git repository tracking.

---

## Cloud Infrastructure Components
* **Compute:** 1 vCPU core (Intel Xeon E312xx @ 2.0GHz) and 1.9 GiB total RAM.
* **Storage:** 19 GiB main root drive (`/dev/vda1`), 881 MiB boot drive, and 105 MiB EFI partition.
* **Networking:** Primary adapter `enp1s0` with private IP `172.30.1.2/24` and an active `docker0` bridge.
* **Operating System:** Ubuntu 24.04.4 LTS running on Linux Kernel 6.8.0-136-generic.

---

## Tools Used
* **KillerCoda:** Online Linux terminal playground used for running system commands.
* **Visual Studio Code:** Code editor used for writing and updating Markdown documentation.
* **Git & GitHub:** Used for tracking lab updates and pushing files to the online repo.
* **Excalidraw:** Online diagram tool used to draw the cloud architecture flowchart.

---

## Linux Commands Executed
* `hostnamectl` – Checked OS name, architecture, kernel version, and KVM virtualization.
* `lscpu` – Inspected CPU model name, clock speed, core counts, and cache sizes.
* `free -h` – Checked available RAM, used memory, and swap space status.
* `df -h` – Inspected disk storage capacity, partition sizes, and usage percentages.
* `ip a` – Displayed active network adapters, IP addresses, and MAC addresses.

---

## Skills Learned
* Reading and understanding raw terminal outputs to check server specs.
* Translating basic Linux system metrics into cloud computing concepts.
* Matching equivalent cloud services across major providers (AWS, Azure, GCP).
* Writing clean technical documentation and creating readable system diagrams.

---

## Challenges Encountered
* **Terminal Disconnections:** The KillerCoda terminal occasionally dropped connection showing a "Reconnecting..." status, which I fixed by refreshing the browser tab.
* **Metric Alignment:** Making sure exact server specs (like CPU details and IP addresses) were accurate and matched across all reports and diagrams.