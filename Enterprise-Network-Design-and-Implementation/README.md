# Project 8 - Enterprise Network Design and Implementation

## Objective

Design and implement a multi-site enterprise network connecting a Head Office and a Branch Office using Cisco Packet Tracer with VLANs, Router-on-a-Stick, OSPF, DHCP, DNS, and Extended ACLs.

---

## Network Topology

![Topology](topology.PNG)

---

## Devices Used

- 2 × Cisco 2911 Routers
- 2 × Cisco 2960 Switches
- 1 × Server
- Multiple PCs

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- VLANs
- Router-on-a-Stick
- OSPF
- DHCP
- DNS
- Extended ACL
- Inter-VLAN Routing

---

## VLAN Configuration

| VLAN | Department | Network |
|------|------------|----------------|
| 10 | HR | 192.168.10.0/24 |
| 20 | IT | 192.168.20.0/24 |
| 30 | Sales | 192.168.30.0/24 |
| 40 | Marketing | 192.168.40.0/24 |
| 60 | Branch Office | 192.168.60.0/24 |

---

## Configuration

### Head Office

- Configured VLANs for HR, IT, Sales and Marketing
- Configured Router-on-a-Stick using IEEE 802.1Q
- Configured DHCP Server
- Configured DNS Server
- Configured OSPF Area 0

### Branch Office

- Configured Branch VLAN
- Connected to Head Office using OSPF
- Configured DHCP Relay (ip helper-address)

### Security

- Configured Extended ACL
- HR and IT can communicate with all departments
- Sales and Marketing are restricted from accessing HR
- Sales and Marketing can communicate with each other

---

## Verification

Verify routing

```bash
show ip route
show ip ospf neighbor
```

Verify VLANs

```bash
show vlan brief
show interfaces trunk
```

Verify DHCP

```bash
show ip dhcp binding
```

Verify ACL

```bash
show access-lists
```

Verify Connectivity

```cmd
ping
ipconfig
```

---

## Skills Learned

- Enterprise Network Design
- VLAN Configuration
- Router-on-a-Stick
- Inter-VLAN Routing
- OSPF Dynamic Routing
- DHCP Configuration
- DHCP Relay (ip helper-address)
- DNS Configuration
- Extended ACL
- Cisco IOS CLI
- Enterprise Network Troubleshooting

---

## Outcome

Successfully designed and implemented a secure multi-site enterprise network with centralized DHCP and DNS services, dynamic routing using OSPF, VLAN segmentation, Router-on-a-Stick, and Extended ACLs. Verified end-to-end connectivity and enforced departmental access policies through comprehensive network testing.
