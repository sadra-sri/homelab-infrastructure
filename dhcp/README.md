# DHCP Configuration Lab

This section documents the configuration and validation of a DHCP server within an Active Directory environment.

---

## Environment

- Server: Windows Server 2022
- Role: DHCP Server
- Domain: lab.local
- Network: Host-only (isolated lab network)

---

## What was done

- Installed the DHCP Server role
- Created a DHCP scope:
  - Range: 192.168.23.50 – 192.168.23.80
- Activated the scope
- Authorized the DHCP server in Active Directory
- Configured DNS option to point to the Domain Controller

---

## Issue Encountered (Important)

Initially, clients were not receiving IP addresses from the DHCP server.

### Root Cause

Clients were connected to a NAT/bridged network, which already had another DHCP service.

As a result, IP addresses were assigned by VMware instead of the configured DHCP server.

---

## Solution

- Created a dedicated Host-only network (VMnet3)
- Disabled VMware DHCP on that network
- Connected all machines (ESXi and clients) to VMnet3
- Ensured all systems were on the same isolated network

---

## Validation

The following checks were performed:

- Verified IP assignment using: ipconfig
- Confirmed IP range matched DHCP scope
- Renewed IP using: ipconfig /renew
- Verified DNS settings from DHCP
- Checked active leases in DHCP console

---

## Screenshots

The following screenshots are included in the screenshots folder:

- DHCP scope configuration
- Active leases
- ipconfig output from client
- DHCP console showing assigned IPs

---

## Outcome

Clients successfully received IP addresses from the DHCP server, confirming correct configuration and network isolation.
