# Project-Networkwalks-Week-1

**Project: Cybersecurity Lab Environment Setup**  
**Type: Internship Task – Week 1**  
**Batch:** B083

---

# Cybersecurity Lab Environment Setup

<p align="center">
  <img src="https://img.shields.io/badge/Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/VirtualBox-v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
</p>

---

## Overview

This project documents the complete setup of a cybersecurity testing lab using **Oracle VirtualBox** and **Kali Linux**.

A custom NAT Network was created using the `10.0.0.0/24` subnet. Kali Linux was imported into VirtualBox, configured with the required network settings, network connectivity was verified, and a VM snapshot was taken after completing the setup.

---

## Lab Configuration

| Component          | Configuration                          |
|--------------------|----------------------------------------|
| Virtualization     | Oracle VirtualBox 7.2.20               |
| Guest OS           | Kali Linux 2026.2                      |
| Network Type       | NAT Network                            |
| Network Name       | NatNetwork                             |
| IPv4 Prefix        | 10.0.0.0/24                            |
| Kali Linux IP      | 10.0.0.2/24                            |
| Gateway            | 10.0.0.1                               |
| DNS                | 8.8.8.8                                |
| VM RAM             | 2048 MB                                |
| VM Disk            | 80.09 GB                               |

---

## Setup Steps

### Step 1: Download and Install 7-Zip
Installed **7-Zip 26.03 (x64)** to extract the Kali Linux virtual machine files.

**Installation Path:**  
`C:\Program Files\7-Zip`

![Step 1 - 7-Zip Installation](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%201%20-%207%20Zip%20Installing.png)

### Step 2: Download and Install VirtualBox
Installed **Oracle VirtualBox 7.2.20 (amd64)** for running the Kali Linux virtual machine.

![Step 2 - VirtualBox Installation](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%202%20-%20Virtual%20Box.png)

### Step 3: Create the NAT Network
Created a custom NAT Network in VirtualBox with the required subnet.

- **Network Name:** NatNetwork  
- **IPv4 Prefix:** 10.0.0.0/24  
- **DHCP:** Enabled  

![Step 3 - NAT Network Configuration](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%203%20-%20VirtualBox%20Natnetwork.png)

### Step 4: Import Kali Linux into VirtualBox
Imported the pre-built **Kali Linux 2026.2 VirtualBox image** into VirtualBox.

- **Name:** kali-linux-2026.2-virtualbox-amd64  
- **OS:** Debian (64-bit)  
- **RAM:** 2048 MB  
- **Disk:** 80.09 GB  

**1. Kali Linux VM Setup**

![Step 4.1 - Kali Linux VM Setup](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%204%20-%20Installing%20Kali%20Linux%20and%20setup.png)

**2. Network Settings**

![Step 4.2 - Network Settings](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%204%20-%20settings%20Network.png)

**3. Kali Linux VM**

![Step 4.3 - Kali Linux VM](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%204%20-kali%20linux.png)

### Step 5: Configure the Kali Linux Network
Configured the Kali Linux virtual machine to use the created NAT Network.

**Network Adapter Settings:**
- Enabled  
- Attached to: **NAT Network**  
- Network: **NatNetwork**  
- Adapter Type: Intel PRO/1000 MT Desktop  
- Promiscuous Mode: Allow All  
- Virtual Cable Connected: Enabled  

**Kali Linux IP Configuration:**
- Address: `10.0.0.2`  
- Netmask: `24`  
- Gateway: `10.0.0.1`  
- DNS: `8.8.8.8`  

![Step 5 - Connecting Ethernet with VirtualBox NAT Network](https://raw.githubusercontent.com/ImYasir02/Project-Networkwalks-Week-1/7f087ac2abf3548732b063c92841aa6efcc18edd/Task%20-%205%20connecting%20ethernet%20with%20%20virtualbox%20natnetwork.png)

### Step 6: Verify Network Configuration

Verified the network interface and IP configuration using:

```bash
ip a 
