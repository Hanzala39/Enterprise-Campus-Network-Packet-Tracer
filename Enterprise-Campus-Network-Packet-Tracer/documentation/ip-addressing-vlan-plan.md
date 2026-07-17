# IP Addressing and VLAN Plan

## Overview

The enterprise campus network uses private Class C IPv4 addressing with VLAN-based segmentation.

Each department is assigned a separate VLAN and IP network to provide logical separation and allow controlled inter-VLAN routing through the Core Layer 3 Switch.

---

# VLAN Design

| VLAN ID | Name | Network | Purpose |
|---------|------|---------|---------|
| 10 | HR | 192.168.10.0/24 | HR user devices |
| 20 | FINANCE | 192.168.20.0/24 | Finance user devices |
| 30 | IT | 192.168.30.0/24 | IT user devices |
| 50 | SERVERS | 192.168.50.0/24 | DHCP, DNS, Web services |

---

# Department IP Addressing

## VLAN 10 - HR Department

Network:

192.168.10.0/24


Default Gateway:


192.168.10.1


End Devices:

| Device | IP Address |
|--------|------------|
| HR-PC1 | 192.168.10.10 |
| HR-PC2 | 192.168.10.11 |
| HR-PC3 | 192.168.10.12 |

---

## VLAN 20 - Finance Department

Network:


192.168.20.0/24


Default Gateway:


192.168.20.1


End Devices:

| Device | IP Address |
|--------|------------|
| FIN-PC1 | 192.168.20.10 |
| FIN-PC2 | 192.168.20.11 |
| FIN-PC3 | 192.168.20.12 |

---

## VLAN 30 - IT Department

Network:


192.168.30.0/24


Default Gateway:


192.168.30.1


End Devices:

| Device | IP Address |
|--------|------------|
| IT-PC1 | 192.168.30.10 |
| IT-PC2 | 192.168.30.11 |
| IT-PC3 | 192.168.30.12 |

---

# VLAN 50 - Server Network

Network:


192.168.50.0/24


Default Gateway:


192.168.50.1


Server Devices:

| Server | IP Address | Service |
|--------|------------|---------|
| DHCP Server | 192.168.50.10 | DHCP |
| DNS Server | 192.168.50.20 | DNS |
| Web Server | 192.168.50.30 | HTTP |

---

# Layer 3 Gateway Assignment

The Cisco Catalyst 3560 Core Switch provides default gateway services using Switch Virtual Interfaces (SVIs).

| VLAN | SVI Address |
|------|-------------|
| VLAN 10 | 192.168.10.1 |
| VLAN 20 | 192.168.20.1 |
| VLAN 30 | 192.168.30.1 |
| VLAN 50 | 192.168.50.1 |

---

# Network Communication

Traffic flow:


HR VLAN
192.168.10.0/24
|
|
CORE-SW
|
|
Finance VLAN IT VLAN Server VLAN
192.168.20.0 192.168.30.0 192.168.50.0


The Core Layer 3 Switch performs inter-VLAN routing between departments and provides access to network services hosted in the Server VLAN.