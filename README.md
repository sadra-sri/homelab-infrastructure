# Enterprise Home Lab using ESXi

This project demonstrates the design and implementation of a virtual enterprise IT infrastructure using VMware ESXi.

The lab simulates a real-world environment including Active Directory, DNS, DHCP, and domain-joined clients, all running in a controlled and isolated network.

---

## 🧠 Overview

This lab was built to gain hands-on experience with core system administration concepts and enterprise infrastructure.

It includes:

- Active Directory Domain Services (AD DS)
- DNS configuration and name resolution
- DHCP setup and troubleshooting
- Domain-joined Windows clients
- Network isolation using Host-only networking
- Nested virtualization using ESXi on VMware Workstation

---

## 🏗️ Architecture

```text
                [ VMware Workstation (Host) ]
                         │
         ┌───────────────┴───────────────┐
         │                               │
 ┌─────────────────────┐        ┌────────────────────────┐
 │        ESXi         │        │   External Client VM   │
 │ (Nested Hypervisor) │        │   (Windows 10)         │
 └─────────┬───────────┘        └───────────┬────────────┘
           │                                │
           │        VMnet3 (Host-only Network)
           └───────────────┬────────────────┘
                           │
                ┌──────────┴──────────┐
                │                     │
        ┌──────────────┐     ┌──────────────┐
        │ Domain Ctrl  │     │  Client VM   │
        │ (AD, DNS,    │     │ (Windows 10) │
        │  DHCP)       │     │              │
        └──────────────┘     └──────────────┘
