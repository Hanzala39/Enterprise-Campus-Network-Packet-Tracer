# Testing and Verification

## Overview

This document verifies the functionality of the enterprise campus network.

Testing was performed in Cisco Packet Tracer to confirm VLAN segmentation, Layer 3 routing, server connectivity, DHCP services, DNS resolution, web access, and firewall operation.

---

# VLAN Verification

## VLAN Implementation

The following VLANs were verified:

| VLAN ID | Name | Network | Status |
|---------|------|---------|--------|
| 10 | HR | 192.168.10.0/24 | Operational |
| 20 | FINANCE | 192.168.20.0/24 | Operational |
| 30 | IT | 192.168.30.0/24 | Operational |
| 50 | SERVERS | 192.168.50.0/24 | Operational |

Result:

All department and server VLANs are active and correctly assigned to their respective switches.

---

# Trunk Connectivity Verification

Trunk links were verified between the Core Layer 3 Switch and access switches.

Verified connections:


CORE-SW
|
|---- HR-SW
|
|---- FIN-SW
|
|---- IT-SW
|
|---- SW4-Server


Result:

All required VLAN traffic is successfully transported between the Core Switch and access layer switches.

---

# Inter-VLAN Routing Verification

The Cisco Catalyst 3560 Core Switch provides Layer 3 routing between VLANs.

Verified networks:

| VLAN | Network | Gateway |
|------|---------|---------|
| 10 | 192.168.10.0/24 | 192.168.10.1 |
| 20 | 192.168.20.0/24 | 192.168.20.1 |
| 30 | 192.168.30.0/24 | 192.168.30.1 |
| 50 | 192.168.50.0/24 | 192.168.50.1 |

Result:

Devices from different VLANs can communicate through the Core Switch.

---

# End Device Connectivity Testing

## HR VLAN Test

Source:


HR-PC1
IP: 192.168.10.10


Destination:


HR Gateway
192.168.10.1


Result:

Successful communication.

---

## Finance VLAN Test

Source:


FIN-PC1
IP: 192.168.20.10


Destination:


192.168.20.1


Result:

Successful communication.

---

## IT VLAN Test

Source:


IT-PC1
IP: 192.168.30.10


Destination:


192.168.30.1


Result:

Successful communication.

---

# Inter-VLAN Communication Test

Test performed between department networks.

Examples:


HR-PC1
192.168.10.10

to

FIN-PC1
192.168.20.10


Result:

Successful communication through Layer 3 routing.

---

# Server VLAN Verification

Server network:


192.168.50.0/24


Connected through:


SW4-Server


Verified services:

| Server | IP Address | Service |
|--------|------------|---------|
| DHCP Server | 192.168.50.10 | DHCP |
| DNS Server | 192.168.50.20 | DNS |
| Web Server | 192.168.50.30 | HTTP |

Result:

All servers are reachable from authorized VLANs.

---

# DHCP Verification

DHCP service was tested using client devices.

Verified clients:

- HR PCs
- Finance PCs
- IT PCs

Expected address ranges:

| VLAN | DHCP Network |
|------|--------------|
| HR | 192.168.10.0/24 |
| Finance | 192.168.20.0/24 |
| IT | 192.168.30.0/24 |

Result:

Clients successfully receive IP addresses from the DHCP server located in VLAN 50.

---

# DNS Verification

DNS Server:


192.168.50.20


Testing:

Client devices successfully communicate with the DNS server and resolve configured names.

Result:

DNS service is operational.

---

# Web Server Verification

Web Server:


192.168.50.30


Testing:

Accessed using a client browser.

Result:

Web service is reachable and operational.

---

# Firewall Verification

Device:


Cisco ASA 5505


Verified features:

- NAT/PAT
- ACL filtering
- Inside/outside traffic control

Result:

Firewall successfully controls traffic between external and internal networks.

---

# Routing Verification

Routing technologies implemented:

- Static routing
- Default route
- OSPF routing

Result:

Routing between network segments is operational.

---

# Final Verification Summary

| Feature | Status |
|---------|--------|
| VLAN Segmentation | PASS |
| Trunk Connectivity | PASS |
| Inter-VLAN Routing | PASS |
| DHCP Service | PASS |
| DNS Service | PASS |
| Web Server Access | PASS |
| Firewall Operation | PASS |
| Routing Functionality | PASS |

The enterprise campus network is fully operational according to the designed architecture.