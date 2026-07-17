# Core Switch - Cisco Catalyst 3560

## Device Role

The Core Switch is the central Layer 3 device for the enterprise campus network.


Responsibilities:

- Inter-VLAN routing
- Default gateway services
- Routing between departments
- Connection between access switches and firewall


---

# Connection to Firewall


Interface:

FastEthernet0/1


Mode:

Layer 3 routed port


IP Address:

192.168.254.2/30


Connected Device:

ASA 5505 Inside Interface


ASA IP:

192.168.254.1/30


---

# Routing

Layer 3 routing enabled:

ip routing


Default route:


Destination:

0.0.0.0/0


Next Hop:

192.168.254.1


Purpose:

Send Internet-bound traffic to ASA firewall.


Command:

ip route 0.0.0.0 0.0.0.0 192.168.254.1


---

# Planned VLAN Architecture


| VLAN | Department | Network |
|---|---|---|
|10|HR|192.168.10.0/24|
|20|Finance|192.168.20.0/24|
|30|IT|192.168.30.0/24|
|50|Servers|192.168.50.0/24|
|99|Management|192.168.99.0/24|


---

# Planned Features


Switching:

- VLANs
- Trunking
- STP
- EtherChannel


Routing:

- Inter-VLAN routing
- OSPF multi-area
- Default route advertisement


Security:

- ACL implementation


Services:

- DHCP relay
- DNS connectivity
- Web server access


---

# Verification Commands

show ip interface brief

show ip route

show running-config


Testing:

ping 192.168.254.1


---

# Project Phase

Completed:

✅ Layer 3 enablement  
✅ ASA connection  
✅ Default route toward firewall