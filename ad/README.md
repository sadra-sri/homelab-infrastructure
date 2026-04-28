# Active Directory

This project demonstrates a simple Active Directory lab using Windows Server 2022 and a Windows 10 client.
It covers installing AD DS, creating a domain, adding Organizational Units (OUs) and users, and joining a client machine to the domain.

Steps Performed
Installed Windows Server 2022 and configured a static IP.
Installed Active Directory Domain Services (AD DS) role.
Promoted the server to a Domain Controller for the domain lab.local.
Created an Organizational Unit (OU) and a test user account.
Joined a Windows 10 client to the lab.local domain.
Verified login and connectivity with the domain user.
Screenshots
AD DS Installed in Server Manager
Server Manager

Active Directory OU and User
ADUC User

Ping test between Client and Domain (lab.local)
![Ping Test](screenshots/03_client & server_ping.png)

Verification with whoami on Client
Whoami

Tools Used
Windows Server 2022 (Domain Controller)
Windows 10 (Client)
VMware Workstation / VirtualBox
Active Directory Domain Services (AD DS)
Purpose
This lab was created to practice real-world IT support and networking scenarios, including domain setup, user management, and troubleshooting.
It serves as a portfolio project to demonstrate practical IT skills.
