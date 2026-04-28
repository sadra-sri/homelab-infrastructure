# Active Directory Home Lab

This project demonstrates the deployment and configuration of an Active Directory environment using Windows Server 2022 and a Windows 10 client within a virtualized lab.

The lab covers the full process of setting up a domain, managing users and Organizational Units (OUs), and joining a client machine to the domain.

---

## Steps Performed

1. Installed Windows Server 2022 and configured a static IP address.
2. Installed the Active Directory Domain Services (AD DS) role.
3. Promoted the server to a Domain Controller for the domain `lab.local`.
4. Created Organizational Units (OUs) and a test user account.
5. Joined a Windows 10 client to the `lab.local` domain.
6. Verified successful login and domain connectivity.

---

## Validation

- Verified domain join from the client machine
- Tested connectivity using `ping`
- Confirmed logged-in domain user using `whoami`

---

## Tools & Technologies

- Windows Server 2022 (Domain Controller)
- Windows 10 (Client)
- Active Directory Domain Services (AD DS)
- Virtualization (VMware)

---

## Purpose

This lab was designed to simulate real-world IT support and system administration tasks, including domain deployment, user management, and troubleshooting.

It also serves as a portfolio project to demonstrate hands-on experience with enterprise IT infrastructure.
