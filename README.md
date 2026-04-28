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
```

---

## ⚙️ Technologies Used

- VMware ESXi (nested on VMware Workstation)
- Windows Server 2022
- Windows 10
- Active Directory (AD DS)
- DNS Server
- DHCP Server

---

## 🔧 Key Features

- Built a complete Active Directory environment from scratch
- Configured DNS for domain name resolution
- Implemented DHCP with proper scope and IP assignment
- Joined clients to the domain
- Applied Group Policy for centralized management
- Designed an isolated lab network to avoid conflicts
- Troubleshot real DHCP conflict issues

---

## 🧪 Validation

The lab was validated using:

- ipconfig (DHCP verification)
- nslookup (DNS resolution)
- ping (connectivity testing)
- whoami (domain authentication)

---

## 📸 Screenshots

Screenshots are available in the /screenshots directory and include:

- ESXi interface  
- Virtual machines  
- DHCP leases  
- DNS configuration  
- Domain login  

---

## 📁 Project Structure

```
ad/
dns/
dhcp/
gpo/
esxi/
clients/
screenshots/
diagrams/
```

---

## 🧠 Key Learnings

- Understanding how AD, DNS, and DHCP work together
- Troubleshooting DHCP conflicts in virtual environments
- Importance of network isolation in lab environments
- Managing users and policies in Active Directory
- Working with nested virtualization

---

## 🎯 Outcome

Successfully built a fully functional enterprise-like lab environment, demonstrating practical system administration and networking skills.

This project reflects hands-on experience relevant to IT Support and System Administration roles.
