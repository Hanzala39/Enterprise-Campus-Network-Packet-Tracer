# SW3 - IT Access Switch

## Device Role

Cisco Catalyst 2960 access layer switch for the IT department.

Provides network connectivity for IT staff and technical resources.

---

# Department Information

Department:

Information Technology (IT)

VLAN ID:

30

VLAN Name:

IT

Network:

192.168.30.0/24

Default Gateway:

192.168.30.1

---

# Connected End Devices

IT User PCs:

- IT-PC1
- IT-PC2
- IT-PC3


---

# Access Port Configuration

User ports are assigned to IT VLAN.


Example:

interface range fa0/1-10

switchport mode access

switchport access vlan 30


---

# Uplink Connection

Connected Device:

Core Switch 3560


Uplink Port:

GigabitEthernet0/1


Connection:

802.1Q Trunk


Purpose:

Carry VLAN traffic to the Layer 3 core switch for routing.


---

# Switching Features

Configured / Planned:

- VLAN assignment
- Access ports
- Trunking
- STP
- EtherChannel
- Port Security


---

# IT Department Role

The IT VLAN may have higher administrative privileges.

Future security policies may allow:

- Network management access
- Device administration
- Monitoring systems


---

# STP

Purpose:

Prevent Layer 2 loops and maintain network stability.


Verification:

show spanning-tree


---

# Port Security

Purpose:

Restrict unauthorized devices from connecting to IT network ports.


Features:

- Sticky MAC addresses
- Maximum MAC limit
- Shutdown violation


Verification:

show port-security interface fa0/1


---

# Verification Commands

show vlan brief

show interfaces trunk

show spanning-tree

show mac address-table


---

# Project Status

Completed:

✅ IT VLAN design  
✅ Access switch planning  

Planned:

⬜ VLAN configuration  
⬜ Trunk configuration  
⬜ STP configuration  
⬜ Port security