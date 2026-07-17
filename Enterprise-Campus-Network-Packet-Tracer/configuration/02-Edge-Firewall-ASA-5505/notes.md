# Edge Firewall - Cisco ASA 5505

## Device Role

The ASA 5505 acts as the security boundary between:

- External Internet network
- Internal enterprise campus network


Main functions:

- Firewall protection
- Security zone separation
- NAT/PAT
- Access control
- Internet gateway


# Network Design


                 ISP Router

              203.0.113.1

                    |

                    |

              ASA 5505

                    |

                    |

              Core 3560 Switch



---

# Interfaces


## Outside Interface

Purpose:

Internet-facing interface


Physical Port:

Ethernet0/0


ASA VLAN:

VLAN 2


Interface Name:

outside


Security Level:

0


IP Address:

203.0.113.2/30


Connected Device:

ISP Router Gi0/0


---

## Inside Interface

Purpose:

Trusted enterprise network connection


Physical Port:

Ethernet0/1


ASA VLAN:

VLAN 1


Interface Name:

inside


Security Level:

100


IP Address:

192.168.254.1/30


Connected Device:

Core 3560 Switch Fa0/1


---

# Security Zones

## Outside

Security level:

0


Meaning:

Untrusted Internet side.


Traffic entering from outside is restricted by default.



## Inside

Security level:

100


Meaning:

Trusted internal company network.


Traffic from inside to outside is allowed by default.


---

# Routing

Default route:

Destination:

0.0.0.0/0


Next Hop:

203.0.113.1


Purpose:

Forward unknown traffic toward the ISP.


Command:

route outside 0.0.0.0 0.0.0.0 203.0.113.1


---

# Future Security Features

Planned:

- NAT/PAT
- ACL filtering
- Internet access control


---

# Verification Commands

show interface ip brief

show route

show running-config


Testing:

ping 203.0.113.1

ping 8.8.8.10


---

# Project Phase

Completed:

✅ ASA placement  
✅ Outside interface configuration  
✅ Inside interface configuration  
✅ Security zones  
✅ Default route