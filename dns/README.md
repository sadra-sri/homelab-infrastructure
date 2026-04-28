# DNS Configuration Lab

This section documents the configuration and validation of DNS within an Active Directory environment.

---

## Environment

- Server: Windows Server 2022
- Role: DNS Server
- Domain: lab.local
- Network: Host-only (isolated lab network)

---

## What was done

- DNS role was installed alongside Active Directory
- Verified that the domain zone (lab.local) was created
- Confirmed the Domain Controller registered automatically in DNS
- Configured clients to use the Domain Controller as their DNS server

---

## Key Configuration

- Forward Lookup Zone: lab.local
- DNS Server IP: 192.168.248.5
- Clients configured to use this DNS server via DHCP

---

## Validation

The following tests were performed:

- Verified DNS resolution using: nslookup
- Confirmed domain name resolution (lab.local)
- Tested hostname resolution of the Domain Controller
- Verified connectivity using ping with hostname

---

## Commands Used

nslookup lab.local  
nslookup server-name  
ping lab.local  

---

## Screenshots

The following screenshots are included in the screenshots folder:

- DNS Manager showing lab.local zone
- A record entries in DNS
- nslookup result from client
- ping using domain name

---

## Outcome

DNS was successfully configured and integrated with Active Directory, allowing clients to resolve domain resources correctly.
