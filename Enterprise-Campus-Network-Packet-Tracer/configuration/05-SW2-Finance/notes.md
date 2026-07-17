# SW2 - Finance Access Switch

## Device Role

Cisco Catalyst 2960 access layer switch for the Finance department.

This switch provides secure network access for Finance users.

---

# Department Information

Department:

Finance

VLAN ID:

20

VLAN Name:

FINANCE

Network:

192.168.20.0/24

Default Gateway:

192.168.20.1

---

# Connected End Devices

Finance User PCs:

- FIN-PC1
- FIN-PC2
- FIN-PC3


---

# Access Port Configuration

User ports belong to Finance VLAN.


Example:

interface range fa0/1-10

switchport mode access

switchport access vlan 20


---

# Uplink Connection

Connected Device:

Core Switch 3560


Uplink:

GigabitEthernet0/1


Mode:

Trunk


Purpose:

Transport Finance VLAN traffic between access layer and core layer.


---

# Switching Features

Configured / Planned:

- VLAN 20 assignment
- Access ports
- Trunking
- STP
- EtherChannel
- Port Security


---

# Security Design

Finance traffic is separated from other departments.

Example:

HR users should not directly access Finance resources without ACL permission.


---

# STP

Purpose:

Maintain a loop-free Layer 2 topology.


Verification:

show spanning-tree


---

# Port Security

Purpose:

Protect Finance access ports.


Features:

- Maximum MAC address limit
- Sticky MAC learning
- Violation shutdown


Verification:

show port-security


---

# Verification Commands

show vlan brief

show interfaces trunk

show spanning-tree

show mac address-table


---

# Project Status

Completed:

✅ Finance VLAN design  
✅ Access switch planning  

Planned:

⬜ VLAN configuration  
⬜ Trunk configuration  
⬜ STP configuration  
⬜ Port security