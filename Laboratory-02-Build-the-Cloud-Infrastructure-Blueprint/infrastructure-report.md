# Infrastructure Assessment Report

## Executive Summary
This report documents the cloud infrastructure audit conducted on a Linux instance running within the KillerCoda environment. The goal is to analyze hardware specifications, memory state, storage configurations, and networking setup to serve as the baseline for a cloud infrastructure blueprint.

---

## Linux Server Specifications

* **Operating System:** Ubuntu 24.04.4 LTS
* **Kernel Version:** Linux 6.8.0-136-generic
* **Hostname:** ubuntu
* **Architecture:** x86_64
* **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update) @ 2.0GHz
* **Number of CPU Cores:** 1 Core
* **Virtualization Type:** KVM (Full Virtualization)
* **Total RAM:** 1.9 GiB
* **Disk Capacity:** 19 GiB (`/dev/vda1`)
* **Mounted File Systems:** 
  * `/dev/vda1` mounted on `/` (Root Partition - 30% Used)
  * `tmpfs` mounted on `/run` (191M Total)
  * `tmpfs` mounted on `/dev/shm` (952M Total)
  * `/dev/vda16` mounted on `/boot` (881M Total)
  * `/dev/vda15` mounted on `/boot/efi` (105M Total)
* **IP Address:** `172.30.1.2` (Primary Interface: `enp1s0`)

---

## Technical Audit Commands & Outputs

### 1. System & OS Identification (`hostnamectl`)
* **Operating System:** Ubuntu 24.04.4 LTS
* **Kernel:** 6.8.0-136-generic
* **Virtualization:** KVM

### 2. CPU Architecture Audit (`lscpu`)
* **Vendor ID:** GenuineIntel
* **Model Name:** Intel Xeon E312xx (Sandy Bridge, IBRS update) @ 2.0GHz
* **Architecture:** x86_64
* **CPUs/Cores:** 1 Core (1 Thread per core, 1 Socket)
* **L1d / L1i Cache:** 32 KiB each
* **L2 Cache:** 4 MiB
* **L3 Cache:** 16 MiB

### 3. Memory Status (`free -h`)
* **Total Memory:** 1.9 GiB
* **Used Memory:** 413 MiB
* **Free Memory:** 872 MiB
* **Buff/Cache:** 785 MiB
* **Available Memory:** 1.5 GiB
* **Swap Space:** 1.0 GiB Total (0B Used)

### 4. Disk Storage & File Systems (`df -h`)
* **Primary System Disk (`/dev/vda1`):** 19 GiB Size (5.4 GiB Used, 13 GiB Available - 30% Utilization)
* **Boot Partition (`/dev/vda16`):** 881 MiB Size (117 MiB Used, 703 MiB Available - 15% Utilization)
* **EFI System Partition (`/dev/vda15`):** 105 MiB Size (6.2 MiB Used, 99 MiB Available - 6% Utilization)

### 5. Network Configuration (`ip a`)
* **Loopback (`lo`):** `127.0.0.1/8`
* **Primary Network Interface (`enp1s0`):** IP `172.30.1.2/24` (Broadcast `172.30.1.255`, MAC `0e:a8:a5:3b:4a:3a`)
* **Docker Bridge (`docker0`):** IP `172.17.0.1/16` (MAC `2a:b0:73:fd:67:d1`)

---

## Conclusion
The instance inspected in KillerCoda runs on a single-core Intel Xeon virtual processor with 1.9 GiB of system RAM and a 19 GiB primary root storage volume. This configuration represents a typical lightweight virtual machine used as a compute host in cloud infrastructure architecture.