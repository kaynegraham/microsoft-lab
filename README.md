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

*Screenshots coming soon*

---

### Network Configuration

- Internal virtual network for domain communication
- NAT adapter for internet access
- Domain controller assigned a static IP address
- Client configured to use the domain controller as DNS

*Screenshots coming soon*

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

*Screenshots coming soon*

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
