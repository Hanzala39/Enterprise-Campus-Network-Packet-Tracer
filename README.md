# Enterprise Campus Network Simulation

![Network Topology](screenshots/topology.png)

A Cisco Packet Tracer project that demonstrates the design and implementation of a secure enterprise campus network using a hierarchical architecture. The network includes VLAN segmentation, Layer 3 switching, DHCP, DNS, web services, OSPF routing, and Cisco ASA firewall security.

---

## Overview

This project simulates a small enterprise network built using Cisco networking technologies and best practices. The network is designed using the **Hierarchical Campus Network Model**, providing scalability, security, and efficient traffic management.

### Objectives

- Design a scalable enterprise network
- Implement VLAN-based network segmentation
- Configure Layer 3 inter-VLAN routing
- Deploy DHCP, DNS, and Web services
- Secure the network using Cisco ASA Firewall
- Implement OSPF dynamic routing
- Verify network functionality through testing

---

## Network Architecture

```text
                 Internet
                     │
              Cisco 2911 Router
                     │
             Cisco ASA 5505 Firewall
                     │
        Cisco Catalyst 3560 Core Switch
                     │
      ┌────────┬────────┬────────┐
      │        │        │        │
   HR-SW    FIN-SW    IT-SW   Server Network
      │        │        │
   HR PCs   FIN PCs   IT PCs
```

---

## Technologies Used

- Cisco Packet Tracer
- Cisco Catalyst 3560 (Layer 3 Switch)
- Cisco Catalyst 2960 (Access Switches)
- Cisco 2911 Router
- Cisco ASA 5505 Firewall
- VLANs
- Inter-VLAN Routing
- OSPF
- Static Routing
- DHCP
- DNS
- HTTP Server
- NAT/PAT
- Access Control Lists (ACLs)

---

## VLAN Plan

| VLAN | Department | Network |
|------|------------|---------|
| 10 | HR | 192.168.10.0/24 |
| 20 | Finance | 192.168.20.0/24 |
| 30 | IT | 192.168.30.0/24 |
| 50 | Servers | 192.168.50.0/24 |

---

## Network Features

- Hierarchical enterprise network design
- Layer 3 switching
- VLAN segmentation
- Inter-VLAN routing
- DHCP address allocation
- DNS name resolution
- Internal web hosting
- Cisco ASA firewall security
- NAT/PAT
- OSPF dynamic routing
- IEEE 802.1Q trunking
- End-to-end network verification

---

## Screenshots

### Network Topology

![Topology](screenshots/topology.png)

---

### VLAN Configuration

![VLAN Configuration](screenshots/vlan-design.png)

---

### Inter-VLAN Connectivity Test

![Ping Test](screenshots/ping-test.png)

---

### Web Server Verification

![Web Server](screenshots/web-server.png)

---

## Repository Structure

```text
Enterprise-Campus-Network/
│
├── README.md
├── topology.pkt
├── docs/
│   ├── device-inventory.md
│   ├── ip-addressing-and-vlan-plan.md
│   └── testing.md
│
└── screenshots/
    ├── topology.png
    ├── vlan-design.png
    ├── ping-test.png
    └── web-server.png
```

---

## Documentation

Project documentation includes:

- Device Inventory
- IP Addressing and VLAN Plan
- Testing and Verification

---

## Skills Demonstrated

- Enterprise Network Design
- Cisco Switching
- Cisco Routing
- VLAN Configuration
- Layer 3 Switching
- OSPF Routing
- Cisco ASA Firewall
- DHCP Configuration
- DNS Configuration
- NAT/PAT
- ACL Configuration
- Network Troubleshooting
- Technical Documentation

---

## Future Improvements

- IPv6 Deployment
- HSRP Gateway Redundancy
- EtherChannel
- Rapid Spanning Tree Protocol (RSTP)
- Wireless Network Integration
- SNMP Monitoring
- VPN Remote Access
- AAA Authentication (RADIUS/TACACS+)

---

## Author

**Hanzala Zahid**

This project was developed using **Cisco Packet Tracer** to demonstrate practical skills in enterprise network design, implementation, security, and documentation.
