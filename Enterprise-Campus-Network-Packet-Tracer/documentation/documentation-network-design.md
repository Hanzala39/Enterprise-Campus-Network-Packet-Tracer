# Enterprise Campus Network Design

## Project Overview

This project simulates a medium-sized enterprise campus network using Cisco Packet Tracer.

The goal is to design and implement a secure, scalable network architecture following real enterprise networking concepts.

---

# Network Architecture


                Internet
                   |
             ISP Router 2911
                   |
            ASA 5505 Firewall
                   |
          Core Layer 3 Switch 3560
                   |
    ---------------------------------
    |               |               |
  SW1             SW2             SW3
  HR            Finance            IT






  

---

# Network Layers

## Edge Layer

Device:

Cisco 2911 ISP Router

Purpose:

- Internet simulation
- Public addressing
- External connectivity


---

## Security Layer

Device:

Cisco ASA 5505 Firewall

Purpose:

- Network security boundary
- NAT/PAT
- ACL filtering
- Internet gateway


---

## Core Layer

Device:

Cisco Catalyst 3560 Layer 3 Switch

Purpose:

- Inter-VLAN routing
- Default gateway services
- Campus routing


---

## Access Layer

Devices:

Cisco Catalyst 2960 switches


Departments:

- HR
- Finance
- IT


Purpose:

- Connect end-user devices
- Provide VLAN segmentation


---

# Technologies Implemented

## Switching

- VLANs
- Access ports
- Trunking
- STP
- EtherChannel


## Routing

- Static routing
- Default route
- OSPF multi-area
- Route redistribution


## Services

- DHCP
- DNS
- Web Server


## Security

- ASA Firewall
- NAT/PAT
- ACL
- Port Security


---

# Project Objective

Build practical understanding of enterprise networking concepts covered in CCNA and prepare for real network deployments.



