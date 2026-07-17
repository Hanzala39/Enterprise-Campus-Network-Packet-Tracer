# ISP Router - Cisco 2911

## Device Role

The ISP Router represents the Internet Service Provider in the enterprise network simulation.

It provides:

- External network connectivity
- Public IP addressing
- Internet path simulation
- Default route toward the enterprise firewall


## Network Connections

### Connection to Internet Server

Interface:

GigabitEthernet0/1

IP Address:

8.8.8.1/24


Connected Device:

Internet Server

IP:

8.8.8.10/24


---

### Connection to Enterprise Firewall

Interface:

GigabitEthernet0/0

IP Address:

203.0.113.1/30


Connected Device:

ASA 5505 Outside Interface

ASA IP:

203.0.113.2/30


---

## Routing Configuration

Static route added:

Destination:

192.168.0.0/16


Next Hop:

203.0.113.2


Purpose:

Allows ISP router to return traffic back toward the internal company networks through the ASA firewall.


## Verification Commands

show ip interface brief

show ip route

ping 8.8.8.10

ping 203.0.113.2


## Project Phase

Completed:

✅ ISP connectivity  
✅ Public IP addressing  
✅ Internet simulation  
✅ Return route toward enterprise network