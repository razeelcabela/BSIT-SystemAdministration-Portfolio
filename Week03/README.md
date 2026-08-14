# Week 3 – Enterprise Server Deployment and Operating System Installation

## Project Overview

This project focuses on installing and configuring Ubuntu Server using Oracle VirtualBox. It also covers server verification, BIOS and UEFI, the Ubuntu boot process, Windows Server installation, and a comparison of enterprise server operating systems.

## Learning Objectives

* Install and configure Ubuntu Server.
* Configure networking, storage, hostname, and SSH.
* Verify server functionality using Linux commands.
* Understand BIOS, UEFI, and the Linux boot process.
* Install Windows Server Evaluation.
* Compare Windows Server, Ubuntu Server, and Rocky Linux.

## Virtual Machine Specifications

| Component | Configuration        |
| --------- | -------------------- |
| VM Name   | Ubuntu-Server-Week03 |
| RAM       | 4 GB                 |
| CPU       | 2 Virtual Processors |
| Storage   | 40 GB                |
| Network   | NAT                  |
| Hostname  | server01             |
| OS        | Ubuntu Server LTS    |

## Installation Summary

Ubuntu Server was installed successfully using Oracle VirtualBox. The installation included DHCP networking, guided disk configuration, a non-root administrative account, the hostname `server01`, and OpenSSH Server.

Windows Server Evaluation was also installed in a separate virtual machine as part of the Week 3 activity.

## Configuration Summary

* **Hostname:** `server01`
* **Network:** DHCP / NAT
* **Storage:** 40 GB
* **Filesystem:** ext4
* **SSH:** OpenSSH Server
* **User Account:** Non-root administrative user

## Verification Results

The Ubuntu Server installation was verified using:

```bash
hostname
ip addr
ping -c 4 google.com
sudo apt update
sudo apt upgrade -y
systemctl status ssh
```

The server successfully connected to the network, received an IP address, accessed the internet, and ran the SSH service.

## BIOS vs UEFI Highlights

BIOS is an older firmware technology, while UEFI is the modern standard used by most computers today. UEFI provides better support for modern storage, GPT partitioning, Secure Boot, and newer hardware.

## Boot Process Flowchart

![Ubuntu Boot Process](diagrams/BootProcessFlowchart.png)

**Boot Process:**

Power On → BIOS/UEFI → Boot Device Detection → GRUB → Linux Kernel → init/systemd → Services Start → Login Prompt

## Challenges Encountered

Some challenges encountered during the activity included:

* Understanding that Linux passwords do not appear while being typed.
* Correctly mounting the Windows Server ISO in VirtualBox.
* Removing the installation ISO after Windows Server installation to prevent the installer from starting again.
* Learning how to send Ctrl+Alt+Delete directly to the Windows Server virtual machine.

## Reflection

This Week 3 activity gave me practical experience in installing and configuring server operating systems using Oracle VirtualBox. I learned that deploying a server involves more than simply installing an operating system. It also requires proper configuration of the virtual hardware, storage, network, hostname, user accounts, and services.

During the Ubuntu Server installation, I learned how to configure DHCP networking, use guided disk partitioning, create an administrative user, assign the hostname `server01`, and install OpenSSH Server. I also became more comfortable using Linux commands. Commands such as `hostname`, `ip addr`, and `ping` helped me verify that the server was configured correctly and connected to the network. I also used APT commands to update the system and `systemctl` to check whether the SSH service was running.

Another important part of the activity was learning about BIOS and UEFI. I learned that UEFI is commonly used in modern computers because it provides better support for modern storage, GPT partitioning, security features such as Secure Boot, and newer hardware. I also learned the basic Ubuntu boot sequence from powering on the computer until the login prompt appears.

Installing Windows Server Evaluation gave me additional experience with virtualization. I encountered problems such as an incorrectly mounted installation ISO and the VM booting into the installer again after installation. Solving these problems helped me understand how virtual optical drives and boot media work.

Overall, this activity improved my understanding of server installation, virtualization, networking, operating systems, Linux commands, and troubleshooting. It also showed me the importance of verifying and documenting every important step when deploying a server.

## References

* Ubuntu Server Documentation – Canonical
* Oracle VirtualBox User Manual – Oracle
* Windows Server Documentation – Microsoft Learn
* Rocky Linux Documentation – Rocky Linux
* UEFI Specifications – UEFI Forum
