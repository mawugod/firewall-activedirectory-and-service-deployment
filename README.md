# Enterprise Security Lab with Oracle VirtualBox
## Perimeter Defense & Identity Management [Firewall, Active Directory & Service Deployment]


[![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=flat-square&logo=virtualbox&logoColor=white)](https://www.virtualbox.org/)
[![Windows Server](https://img.shields.io/badge/Windows%20Server-0078D4?style=flat-square&logo=windows&logoColor=white)](https://www.microsoft.com/en-us/windows-server)
[![pfSense](https://img.shields.io/badge/pfSense-212121?style=flat-square&logo=pfsense&logoColor=white)](https://www.pfsense.org/)
[![Active Directory](https://img.shields.io/badge/Active%20Directory-0078D4?style=flat-square&logo=microsoft&logoColor=white)](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/)

## 📋 Table of Contents

- [Prerequisites](#prerequisites)
- [Phase 1: Network Foundation](#phase-1-network-foundation-5-minutes)
- [Phase 2: pfSense Firewall Setup](#phase-2-pfsense-firewall-setup-10-minutes)
- [Phase 3: Domain Controller Setup](#phase-3-domain-controller-setup-15-minutes)
- [Phase 4: Web Server Setup](#phase-4-web-server-setup-10-minutes)
- [Phase 5: Management PC Setup](#phase-5-management-pc-setup-10-minutes)
- [Phase 6: Port Forwarding Configuration](#phase-6-port-forwarding-configuration-5-minutes)
- [Testing & Validation](#testing--validation-scenarios)
- [Security Concepts](#security-concepts-implemented)
- [Troubleshooting](#troubleshooting-common-issues)
- [Learning Outcomes](#learning-outcomes)

---

## Learning Outcomes

After completing this lab, you will understand:

1. **Enterprise Network Architecture**: How modern networks are structured
2. **Security Perimeter Design**: Implementing defense-in-depth strategies
3. **Identity Management**: Centralized authentication and authorization
4. **Service Deployment**: Hosting services in a secure environment
5. **Administrative Practices**: Proper management of IT infrastructure
6. **Network Security**: Firewall configuration and access control

This lab provides a foundation for understanding enterprise IT security concepts in a hands-on environment.

---
### Key Concepts Implemented

- **Network Segmentation**: Isolating internal network from internet
- **Centralized Authentication**: Active Directory domain services
- **Defense in Depth**: Multiple security layers (firewall + domain security)
- **Principle of Least Privilege**: Controlled access through firewall rules

## Architecture

![image](https://github.com/user-attachments/assets/3771a0df-694e-47d0-9d71-878ddf6f44a3)

### Network Layout

| Device | IP Address | Role | Services |
|--------|------------|------|----------|
| pfSense | 192.168.10.1 | Firewall/Gateway | NAT, Firewall Rules |
| DC01 | 192.168.10.10 | Domain Controller | AD DS, DNS, DHCP |
| WEB01 | 192.168.10.20 | Web Server | IIS, HTTP Services |
| MGMT01 | DHCP (.50-.100) | Management PC | RSAT Tools |

## Prerequisites

- Oracle VirtualBox 6.0 or later
- Windows Server 2019/2022 ISO
- Windows 10 Pro/Enterprise ISO
- pfSense CE ISO
- Minimum 32GB RAM on host system
- 100GB free disk space

---

## Contributing

Feel free to submit issues and enhancement requests! This lab can be extended with additional security components like:

- Certificate Authority (CA) services
- Network monitoring tools
- Additional web applications
- Database servers
- Load balancers

**⚠️ Disclaimer**: This lab is for educational purposes only. Do not use these configurations in production environments without proper security hardening.
