# Enterprise Network Design with ASA Firewall & DMZ

<p align="center">
  <img src="https://img.shields.io/badge/Tool-Cisco%20Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/Firewall-Cisco%20ASA-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white" />
  <img src="https://img.shields.io/badge/Architecture-DMZ-E22C2C?style=for-the-badge&logo=target&logoColor=white" />
  <img src="https://img.shields.io/badge/Protocol-VLAN%20%7C%20NAT%20%7C%20ACL-4B4B4B?style=for-the-badge&logo=cisco&logoColor=white" />
</p>

> Enterprise network infrastructure project for **EvolveIT Tech** — implementing VLAN segmentation, EtherChannel, Cisco ASA firewall, DMZ architecture, static NAT, ACLs, AAA authentication, and secure remote management.

---

## Overview

This project simulates a fully functional enterprise network for a mid-sized technology company. The design focuses on **network security**, **traffic segmentation**, and **secure internet access**, incorporating industry-standard practices used in real corporate environments.

The network was designed and implemented entirely in **Cisco Packet Tracer**, demonstrating practical skills in firewall configuration, DMZ architecture, and access control policy enforcement.

---

## Network Architecture

### Network Zones

| Zone | Purpose | Security Level |
|------|---------|---------------|
| Inside (Internal) | Corporate departments | High (100) |
| DMZ | Public-facing web server | Medium (50) |
| Outside | Internet / untrusted | Low (0) |

### Internal VLANs

| VLAN | Department |
|------|-----------|
| Management VLAN | IT Administration |
| Operations VLAN | Operations Team |
| Marketing VLAN | Marketing Team |

---

## Technologies Implemented

### Firewall & Security
- **Cisco ASA Firewall** — three-interface configuration (Inside / DMZ / Outside)
- **DMZ Web Server** — static NAT for public access with ASA inspection
- **Access Control Lists (ACLs)** — inbound/outbound traffic filtering
- **AAA Authentication** — centralized access control for device management
- **SSH** — encrypted remote management (Telnet disabled)

### Network Design
- **VLANs** — department-level traffic segmentation
- **EtherChannel** — link aggregation for redundancy and throughput
- **PortFast & BPDU Guard** — Spanning Tree security on access ports
- **Inter-VLAN Routing** — Layer 3 switching for VLAN communication

### IP Services
- **DHCP** — dynamic IP assignment per VLAN
- **Static NAT** — DMZ web server public IP mapping
- **PAT (Port Address Translation)** — inside hosts sharing a public IP
- **NTP** — network time synchronization

---

## Key Security Features

- Three-zone firewall design separating Inside, DMZ, and Outside traffic
- DMZ web server accessible from Internet via static NAT, isolated from internal network
- ACLs enforcing least-privilege traffic policies between all zones
- AAA authentication preventing unauthorized device access
- SSH-only remote management — Telnet disabled on all devices
- EtherChannel providing redundant uplinks between switches
- BPDU Guard protecting against rogue switch attacks on access ports

---

## Network Diagram

> See `P2-Business Company Network Design.pdf` for the full topology diagram.

**High-level topology:**

<img width="1780" height="926" alt="image" src="https://github.com/user-attachments/assets/4168fd8f-c861-4b08-8600-ea48631bb64d" />

---

## Implementation Steps

| Step | Task |
|------|------|
| 1 | Network topology design and IP addressing scheme |
| 2 | VLAN creation and trunk/access port configuration |
| 3 | EtherChannel and Spanning Tree security setup |
| 4 | Inter-VLAN routing via Layer 3 switch |
| 5 | DHCP server configuration per VLAN |
| 6 | Cisco ASA firewall deployment and zone configuration |
| 7 | DMZ web server setup with static NAT |
| 8 | ACL creation and application on ASA interfaces |
| 9 | AAA authentication and SSH remote management |
| 10 | PAT configuration for inside-to-outside internet access |
| 11 | End-to-end connectivity testing and verification |

---

## Repository Contents

```
Enterprise-Network-firewall-dmz
├── 📄 README.md
└── 📋 P2-Business Company Network Design.pdf   ← Full project report & topology
```

---

## Skills Demonstrated

`Cisco ASA Firewall` `DMZ Architecture` `VLAN Segmentation` `Network Security` `ACL Configuration` `Static NAT` `PAT` `EtherChannel` `AAA Authentication` `SSH` `Cisco Packet Tracer` `Enterprise Networking` `Security Policy Enforcement`

---

## Real-World Relevance

This design reflects core skills required for:
- **Network Security Engineer** roles — firewall configuration and zone-based security
- **SOC Analyst** roles — understanding network topology for threat detection
- **Security+ / CCNA** exam domains — NAT, ACLs, VLANs, firewall concepts
- **PhD research** in network security — practical implementation of defense-in-depth architecture

---

## Disclaimer

This project was designed and implemented in Cisco Packet Tracer for academic and educational purposes. All company names, IP addresses, and configurations are fictitious.

---

## Author

**Hashan Kodippilige**  
M.S. Cybersecurity — Minnesota State University Moorhead  
📧 hashansharindu@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/hashankodippilige/)  
🐙 [GitHub](https://github.com/hashan-kodippilige)
