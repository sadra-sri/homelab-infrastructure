# Active Directory Domain Services (AD DS) Lab

This module documents the deployment and validation of an Active Directory Domain Services (AD DS) environment using Windows Server 2022 and domain-joined Windows clients, running on VMware ESXi.

---

## Environment

- Hypervisor: VMware ESXi (nested on VMware Workstation)
- Domain: lab.local
- Domain Controller: Windows Server 2022
- Clients: Windows 10 (domain-joined)
- Network: Host-only (isolated lab network)

---

## Objectives

- Deploy a Domain Controller (DC)
- Create and organize directory structure (OUs)
- Manage users and groups
- Join client machines to the domain
- Validate authentication and name resolution

---

## Implementation Steps

1. **Server Preparation**
   - Installed Windows Server 2022
   - Configured static IP address
   - Set DNS to point to itself

2. **AD DS Installation**
   - Installed the *Active Directory Domain Services* role via Server Manager
   - Promoted the server to a Domain Controller

3. **Domain Configuration**
   - Created a new forest: `lab.local`
   - Verified AD DS services and DNS integration

4. **Directory Structure**
   - Created Organizational Units (OUs) for logical separation
   - Created test users and groups

5. **Client Integration**
   - Configured client DNS to use the Domain Controller
   - Joined Windows 10 clients to the domain
   - Verified successful domain login

---

## Validation

- Verified domain join from client systems
- Tested connectivity using `ping`
- Confirmed domain user context using `whoami`
- Verified DNS resolution for domain resources

---

## Key Concepts Demonstrated

- Active Directory architecture (Domain Controller, OU, Users)
- DNS dependency in AD environments
- Client authentication within a domain
- Basic identity and access management

---

## Screenshots

Screenshots are available in the `/screenshots` directory and include:

- AD DS role installation (Server Manager)
- Domain Controller promotion
- Active Directory Users and Computers (OU & Users)
- Domain join configuration on client
- Successful domain login
- Command-line validation (ping, whoami)

---

## Outcome

Successfully deployed a functional Active Directory environment with domain-joined clients, demonstrating core enterprise identity management concepts.
