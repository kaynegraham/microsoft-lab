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

<img width="1135" height="823" alt="serveradapters" src="https://github.com/user-attachments/assets/d562b6b4-f4c4-4233-91ec-3c57d6232602" />
<img width="1212" height="824" alt="serverping" src="https://github.com/user-attachments/assets/f7c74252-54a5-4bcf-89b7-9dd5623520e7" />

---

### 2. Client Domain Join

- Installed Windows 11 Enterprise Evaluation
- Configured DNS to point to the domain controller
- Joined the client to the `lab.local` domain
- Verified domain authentication

*Screenshots coming soon*

---

## Skills Developed

- Windows Server administration
- Active Directory management
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

## Future Improvements

- Create structured Active Directory Organizational Units (OUs)
- Implement basic Group Policy Objects (GPOs)
- Configure shared file resources
- Add additional client machines
- Expand network complexity

---

## Conclusion

This lab provided practical, hands-on experience with enterprise Windows environments and reinforced core IT support concepts used in real-world helpdesk and MSP roles.

This environment will continue to be expanded to support ongoing learning and experimentation.

---
