# Device Inventory

## Overview

This section documents all network devices used in the enterprise campus network simulation.

The inventory includes device models, roles, locations, and primary functions within the architecture.

---

# Network Device Inventory

| Device Name | Model | Layer | Location | Role |
|-------------|-------|-------|----------|------|
| ISP-RTR | Cisco 2911 | Edge Layer | Internet Edge | Provides external connectivity and Internet simulation |
| ASA-FW | Cisco ASA 5505 | Security Layer | Perimeter | Firewall, NAT/PAT, ACL enforcement |
| CORE-SW | Cisco Catalyst 3560 | Core Layer | Main Network Room | Layer 3 switching, inter-VLAN routing, gateway services |
| HR-SW | Cisco Catalyst 2960 | Access Layer | HR Department | User connectivity and VLAN access |
| FIN-SW | Cisco Catalyst 2960 | Access Layer | Finance Department | User connectivity and VLAN access |
| IT-SW | Cisco Catalyst 2960 | Access Layer | IT Department | User connectivity and VLAN access |

---

# End Device Inventory

| Device Name | Device Type | Department | Purpose |
|-------------|-------------|------------|---------|
| HR-PCs | Desktop PCs | HR | Employee workstation access |
| FIN-PCs | Desktop PCs | Finance | Financial application access |
| IT-PCs | Desktop PCs | IT | Network administration and testing |
| WEB-SERVER | Server | Data Services | Internal web hosting |
| DNS-SERVER | Server | Data Services | Name resolution services |
| DHCP-SERVER | Server | Data Services | Dynamic IP address allocation |

---

# Device Roles

## ISP-RTR (Cisco 2911)

Function:

- Simulates the Internet Service Provider connection
- Provides upstream connectivity
- Advertises default route toward enterprise network

Main responsibilities:

- WAN connectivity
- Public IP addressing
- Internet path simulation


---

## ASA-FW (Cisco ASA 5505)

Function:

- Protects internal campus network from external traffic

Security services:

- Stateful firewall inspection
- NAT/PAT translation
- Access Control Lists
- Traffic filtering

Network position:


---

## CORE-SW (Cisco Catalyst 3560)

Function:

- Central Layer 3 routing device
- Provides communication between VLANs

Responsibilities:

- VLAN gateway interfaces
- Inter-VLAN routing
- OSPF routing
- DHCP relay
- Route distribution


---

## Access Switches (Cisco Catalyst 2960)

### HR-SW

Purpose:

- Provides connectivity for HR users
- Assigns HR VLAN membership
- Connects HR workstations


### FIN-SW

Purpose:

- Provides connectivity for Finance users
- Maintains Finance VLAN isolation
- Connects finance workstations


### IT-SW

Purpose:

- Provides connectivity for IT users
- Supports network management devices
- Provides administrative access


---

# Interface Summary

| Device | Connection | Purpose |
|--------|------------|---------|
| ISP-RTR → ASA-FW | WAN Link | Internet handoff |
| ASA-FW → CORE-SW | Inside Link | Protected campus connection |
| CORE-SW → HR-SW | Trunk | HR VLAN transport |
| CORE-SW → FIN-SW | Trunk | Finance VLAN transport |
| CORE-SW → IT-SW | Trunk | IT VLAN transport |

---

# Naming Convention

The following naming standard is used:

| Prefix | Meaning |
|--------|---------|
| RTR | Router |
| FW | Firewall |
| CORE | Core Layer Device |
| SW | Access Switch |
| PC | End User Computer |
| SRV | Server |

Example:



CORE-SW


Meaning:

- CORE = Core layer
- SW = Switch device

---

# Summary

The enterprise campus network consists of:

- 1 Edge Router
- 1 Firewall
- 1 Core Layer 3 Switch
- 3 Access Layer Switches
- Multiple End Devices and Servers

This design follows the hierarchical campus model:


Edge
|
Security
|
Core
|
Access
|
Users





The inventory provides the foundation for configuration, addressing, VLAN planning, and implementation documentation.