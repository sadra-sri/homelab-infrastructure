\# Group Policy Lab – Enforcing Wallpaper via GPO



This project demonstrates the use of \*\*Group Policy Objects (GPOs)\*\* in Active Directory to enforce a desktop wallpaper across all domain-joined clients.



---



\## Steps Performed

1\. On the Domain Controller, created a folder `C:\\Wallpaper` and placed `1.jpg` inside it.

2\. Shared the folder as `\\\\SERVER\_SADRA\\Wallpaper` with \*\*Read\*\* permissions for `Everyone`.

3\. Opened \*\*Group Policy Management Console (GPMC)\*\* and created a new GPO `Wall`.

4\. Edited the GPO under:  

&nbsp;  `User Configuration → Administrative Templates → Desktop → Desktop Wallpaper`

&nbsp;  - Enabled the policy.  

&nbsp;  - Set wallpaper path to: `\\\\SERVER\_SADRA\\Wallpaper\\1.jpg`  

&nbsp;  - Wallpaper style: \*\*Center\*\*

5\. Linked the GPO to the domain (`lab.local`).

6\. On the Windows 10 client:

&nbsp;  - Ran `gpupdate /force`  

&nbsp;  - Logged out and back in → Wallpaper updated successfully.



---



\## Screenshots

\- \*\*Shared Folder with Wallpaper Image\*\*  

&nbsp; !\[Shared Folder](screenshots/01\_shared\_folder.png)



\- \*\*GPO Configured for Desktop Wallpaper\*\*  

&nbsp; !\[GPO Settings](screenshots/02\_gpo\_wallpaper.png)



\- \*\*Client Desktop After Applying GPO\*\*  

&nbsp; !\[Client Wallpaper](screenshots/03\_client\_wallpaper.png)



---



\## Tools Used

\- Windows Server 2022 (Domain Controller)

\- Windows 10 (Client)

\- Active Directory Group Policy Objects (GPO)



---



\## Purpose

This lab was created to practice using \*\*Group Policy\*\* to centrally manage user environments in an Active Directory domain.  

It serves as a \*\*portfolio project\*\* to demonstrate IT support and system administration skills.



