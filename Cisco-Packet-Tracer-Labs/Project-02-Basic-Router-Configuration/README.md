# Project 2 - Basic Router Configuration

## 📌 Objective

Configure a Cisco router to connect two different LANs and enable communication between them using static IPv4 addressing.

---

## 🖥 Network Topology

![Network Topology](topology.jpg)

---

## 🛠 Devices Used

- Cisco 1941 Router
- Cisco 2960 Switch
- 2 PCs

---

## 🌐 IP Addressing

| Device | Interface | IP Address | Subnet Mask |
|---------|-----------|------------|-------------|
| Router | G0/0 | 192.168.10.1 | 255.255.255.0 |
| Router | G0/1 | 192.168.20.1 | 255.255.255.0 |
| PC0 | Fa0 | 192.168.10.10 | 255.255.255.0 |
| PC1 | Fa0 | 192.168.20.10 | 255.255.255.0 |

---

## ⚙ Router Configuration

```bash
enable
configure terminal

interface g0/0
ip address 192.168.10.1 255.255.255.0
no shutdown
exit

interface g0/1
ip address 192.168.20.1 255.255.255.0
no shutdown
exit
```

---

## 💻 PC Configuration

### PC0

- IP Address: 192.168.10.10
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.10.1

### PC1

- IP Address: 192.168.20.10
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.20.1

---

## ✅ Verification

Commands used:

```cmd
ping 192.168.20.10
```

```cmd
ipconfig
```

Router verification:

```bash
show ip interface brief
```

Expected Result:

- Interfaces are **up/up**
- PCs can successfully ping each other through the router.

---

## 📚 Skills Learned

- Cisco IOS CLI
- Router Interface Configuration
- IPv4 Addressing
- Default Gateway Configuration
- Basic Routing
- Connectivity Testing
- Troubleshooting

---

## 🎯 Outcome

Successfully configured a Cisco router to connect two LANs and verified end-to-end connectivity using ICMP (ping).
