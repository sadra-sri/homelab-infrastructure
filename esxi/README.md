# ESXi Virtualization Environment

This section documents the virtualization platform used to build the home lab.

---

## Environment

- Hypervisor: VMware ESXi 7.0
- Deployment Type: Nested (installed on VMware Workstation)
- Host Platform: VMware Workstation (Windows 11)
- Network: VMnet3 (Host-only isolated network)

---

## Lab Architecture

ESXi is used as the main virtualization platform to host all lab machines:

- Domain Controller (Windows Server 2022)
  - Active Directory
  - DNS
  - DHCP

- Windows 10 Clients
  - Domain-joined
  - Receiving IP from DHCP

---

## Storage

- Created a dedicated datastore for virtual machines
- Separated ESXi system disk from VM storage disk

---

## Networking

- Configured an isolated network using VMnet3 (Host-only)
- Avoided NAT/Bridged networks to prevent DHCP conflicts
- Ensured all systems are connected to the same network

---

## What Was Achieved

- Successfully installed ESXi on VMware Workstation (nested virtualization)
- Created and managed virtual machines inside ESXi
- Built a fully isolated lab network
- Integrated ESXi with external client running on Workstation

---

## Validation

- Accessed ESXi web interface successfully
- Verified all VMs are running
- Confirmed communication between server and clients
- Verified DHCP, DNS, and Active Directory functionality

---

## Screenshots

- ESXi web interface
- Virtual machines list
- Datastore configuration
- Network configuration

---

## Outcome

A working ESXi-based lab environment was built inside VMware Workstation to simulate a real-world enterprise infrastructure.
