# Windows Server 2022 Active Directory Home Lab

## Overview

This project documents a Windows home lab built to simulate a small business Active Directory environment. The lab demonstrates core IT support and system administration fundamentals relevant to entry-level helpdesk and MSP environments.

The goal of this lab is to gain hands-on experience with domain controllers, client domain joining, DNS configuration, and shared resource management in a controlled virtual environment.

---

## Lab Architecture

### Environment

- **Hypervisor:** [Oracle VirtualBox](https://www.virtualbox.org/)
- **Server OS:** [Windows Server 2022 Evaluation](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022)
- **Client OS:** [Windows 11 Enterprise Evaluation](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-11-enterprise)
- **Domain:** `lab.local`
  
<img width="948" height="756" alt="Screenshot 2026-02-09 120444" src="https://github.com/user-attachments/assets/28eef2cf-10a7-4bfa-9cbe-5510a277372b" />

---

### Network Configuration

- Internal virtual network for domain communication
- NAT adapter for internet access
- Domain controller assigned a static IP address
- Client configured to use the domain controller as DNS
<img width="955" height="753" alt="hostonly" src="https://github.com/user-attachments/assets/608734bd-201a-4965-a68e-c18eb8b95fc7" />


<img width="943" height="741" alt="nat" src="https://github.com/user-attachments/assets/87aa4351-9f56-4700-81b4-33a322723cec" />

---

## Purpose

This lab was built to develop practical experience with:

- Active Directory Domain Services (AD DS) setup
- DNS configuration and troubleshooting
- Joining Windows clients to a domain
- Virtual network configuration
- Technical documentation and troubleshooting workflow

---

## Implementation Steps

### 1. Domain Controller Setup

- Installed Windows Server 2022
- Installed Active Directory Domain Services
- Promoted the server to a domain controller
- Configured DNS services
- Assigned a static IP address

<img width="1030" height="775" alt="serveradapters" src="https://github.com/user-attachments/assets/b66eb322-8262-4361-92bb-3547416a244c" />


<img width="1212" height="824" alt="serverping" src="https://github.com/user-attachments/assets/f7c74252-54a5-4bcf-89b7-9dd5623520e7" />

---

### 2. Client Domain Join

- Installed Windows 11 Enterprise Evaluation
- Configured DNS to point to the domain controller
- Joined the client to the `lab.local` domain
- Verified domain authentication

<img width="1182" height="846" alt="clientpingserver" src="https://github.com/user-attachments/assets/b0b591ea-a7f2-4ef6-9480-796032dee012" />


<img width="1217" height="846" alt="domainjoin" src="https://github.com/user-attachments/assets/5504f549-2d87-4900-a348-975198fc2b05" />


<img width="1154" height="824" alt="welcometodomain" src="https://github.com/user-attachments/assets/be7ad861-dbe5-4905-a7a3-0136a4e1db80" />

---

### 3. Active Directory Authentication

- Created a domain user account in Active Directory
- Successfully joined Windows 11 client to the domain
- Verified domain login using domain credentials
  
<img width="1202" height="872" alt="createuserinad" src="https://github.com/user-attachments/assets/245a6e6e-f18c-4bba-a955-d15b6059e1ad" />

<img width="1185" height="835" alt="domainuserclient" src="https://github.com/user-attachments/assets/f68fce3c-37f7-49e3-b51d-fae36a38b8e3" />

<img width="1233" height="839" alt="domainloginscreen" src="https://github.com/user-attachments/assets/b8fae576-c985-4c1f-a5be-1a30c75f0fe0" />

---

### 4. Creating Organized Units (OUs)
- Default Active Directory containers doesn't support Group Policy
- Created custom Organizational Units (OUs) at the domain root and moved user and computer objects into them for proper Group Policy scoping.
  
<img width="1156" height="829" alt="domaincomputer" src="https://github.com/user-attachments/assets/dcbcac1d-60ab-47e3-af63-d9265dbcb347" />

<img width="1227" height="874" alt="domainuser" src="https://github.com/user-attachments/assets/1fad9600-e102-4267-b921-e5acb44197f1" />

---

### 5. Creating a Wallpaper Group Policy (GPOs)
- Created folder on Domain Controller with 2 (IT & General Staff) wallpapers in it
- Created Desktop Wallpaper Group Policy to force image as wallpaper
  
<img width="1185" height="848" alt="staffdesktopgpo" src="https://github.com/user-attachments/assets/19e0de67-f8ed-4636-83cb-98e78635a62b" />

<img width="1179" height="883" alt="sharedwallpaperfolder" src="https://github.com/user-attachments/assets/e23db93d-4fed-4547-838a-ada63df10a7b" />

<img width="1245" height="857" alt="staffwallpaper" src="https://github.com/user-attachments/assets/e8d2bab1-d861-4268-b93d-8949d5aa179d" />

<img width="1194" height="859" alt="itwallpaper" src="https://github.com/user-attachments/assets/ad05f170-d263-4c4c-8ec3-3a9914612f2f" />

---
### 6. Create Data-Share Folder (File Share)


---

## Skills Developed

- Windows Server administration
- Active Directory management
- Creating Basic Group Policies
- DNS troubleshooting
- Network configuration
- Virtual lab design
- Technical documentation

---

## Challenges & Troubleshooting

### Windows 11 not joining domain
**Issue:** Client initially failed to join the domain due to incorrect DNS configuration.

**Resolution:** Manually configured the client to use the domain controller as its DNS server, restoring domain communication.

### Windows 11 Upgrade
**Issue:** Windows 11 Home edition could not upgrade to Enterprise for domain joining.

**Resolution:** Performed a clean installation of Windows 11 Enterprise Evaluation ISO to ensure full domain compatibility.

---
