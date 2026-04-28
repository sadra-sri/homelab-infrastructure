# Group Policy Lab – Enforcing Desktop Wallpaper

This project demonstrates the use of Group Policy Objects (GPOs) in Active Directory to centrally enforce a desktop wallpaper across domain-joined clients.

---

## Steps Performed

1. On the Domain Controller, created a folder: C:\Wallpaper and placed an image file (1.jpg) inside it.

2. Shared the folder over the network with read permissions:
\\SERVER\Wallpaper

3. Opened Group Policy Management Console (GPMC) and created a new GPO:
Desktop-Wallpaper-Policy

4. Configured the GPO under:
User Configuration → Administrative Templates → Desktop → Desktop Wallpaper

- Enabled the policy  
- Set wallpaper path: \\SERVER\Wallpaper\1.jpg  
- Set wallpaper style: Center  

5. Linked the GPO to the domain (lab.local).

6. On the Windows 10 client:

- Ran: gpupdate /force  
- Logged out and logged back in → Wallpaper applied successfully  

---

## Validation

- Verified GPO application using gpupdate  
- Confirmed wallpaper change on client machines  
- Verified shared folder accessibility  

---

## Tools & Technologies

- Windows Server 2022 (Domain Controller)  
- Windows 10 (Client)  
- Group Policy Management (GPMC)  
- Active Directory  

---

## Purpose

This lab demonstrates centralized management of user environments using Group Policy in an Active Directory domain.

It serves as a practical example of enforcing configurations across multiple domain-joined systems.
