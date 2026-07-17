# SW1 - HR Access Switch

## Device Role

Cisco Catalyst 2960 access layer switch for the Human Resources department.

This switch provides network connectivity for HR users and connects the HR VLAN to the campus core network.

---

# Department Information

Department:

Human Resources (HR)

VLAN ID:

10

VLAN Name:

HR

Network:

192.168.10.0/24

Default Gateway:

192.168.10.1

---

# Connected End Devices

HR User PCs:

- HR-PC1
- HR-PC2
- HR-PC3


---

# Access Port Configuration

User-facing ports operate as access ports.

Purpose:

Allow end devices to connect only to the HR VLAN.


Example:

interface range fa0/1-10

switchport mode access

switchport access vlan 10


---

# Uplink Connection

Connected Device:

Core Switch 3560


Uplink Port:

GigabitEthernet0/1


Connection Type:

Trunk


Purpose:

Carry VLAN traffic between the access layer and core layer.


Allowed VLANs:

- VLAN 10 HR
- VLAN 20 Finance
- VLAN 30 IT
- VLAN 50 Servers
- VLAN 99 Management


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

# STP Role

Purpose:

Prevent Layer 2 switching loops and broadcast storms.


Verification:

show spanning-tree


---

# Port Security

Purpose:

Prevent unauthorized devices from connecting to HR network ports.


Planned configuration:

- Maximum one MAC address per port
- Sticky MAC learning
- Shutdown violation mode


Verification:

show port-security interface fa0/1


---

# Verification Commands

Check VLAN:

show vlan brief


Check trunks:

show interfaces trunk


Check MAC addresses:

show mac address-table


Check STP:

show spanning-tree


---

# Project Status

Completed:

✅ HR VLAN design  
✅ Access switch planning  

Planned:

⬜ VLAN configuration  
⬜ Trunk configuration  
⬜ STP verification  
⬜ Port security