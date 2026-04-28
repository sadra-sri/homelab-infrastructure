# Domain-Joined Clients

This section documents the setup and validation of Windows client machines joined to the Active Directory domain.

---

## Environment

- OS: Windows 10
- Domain: lab.local
- Domain Controller: Windows Server 2022
- Network: Host-only lab network

---

## What was done

- Client received IP address from DHCP
- DNS was set to the Domain Controller
- Client was joined to the domain (lab.local)
- User logged in using domain credentials

---

## Validation

The following tests were performed:

- Checked IP configuration using: ipconfig
- Renewed IP address using: ipconfig /renew
- Verified connectivity using: ping
- Verified logged-in user using: whoami

---

## Screenshots

The following screenshots are included in the screenshots folder:

- IP configuration (ipconfig)
- Domain join screen
- Login with domain user
- whoami command result
- ping test

---

## Outcome

The client machine successfully connected to the domain and communicated with AD, DNS, and DHCP services.
