# Project 3 - DHCP and DNS Configuration

## 📌 Objective

Configure a Cisco router, switch, and server to provide automatic IP address assignment using DHCP and hostname resolution using DNS.

---

## 🖥 Network Topology

![Topology](topology.png)

---

## 🛠 Devices Used

- Cisco 1941 Router
- Cisco 2960 Switch
- Cisco Server
- PC0
- PC1
- Printer

---

## 🌐 Network Information

| Device | IP Address |
|----------|------------|
| Router G0/0 | 192.168.100.1 |
| Server | 192.168.100.2 |
| PCs | DHCP Assigned |

Subnet Mask

255.255.255.0

Default Gateway

192.168.100.1

DNS Server

192.168.100.2

---

## ⚙ Configuration Summary

### Router

Configured the router interface with:

- IPv4 Address
- Default Gateway
- Enabled Interface

---

### Server

Configured:

- Static IP Address
- DHCP Service
- DNS Service

Created DHCP Pool:

Office

Created DNS Record:

office.local → 192.168.100.2

---

### PCs

Configured to obtain IPv4 settings automatically using DHCP.

---

## 🔍 Verification

### DHCP

```cmd
ipconfig
```

Expected

```text
IP Address : 192.168.100.x
Gateway : 192.168.100.1
DNS : 192.168.100.2
```

---

### Connectivity

```cmd
ping 192.168.100.2
```

Successful reply received.

---

### DNS Resolution

```cmd
ping office.local
```

Successful hostname resolution.

---

## 🧪 Cisco IOS Verification Commands

```bash
show ip interface brief
```

```bash
show running-config
```

---

## 📚 Skills Learned

- DHCP Configuration
- DNS Configuration
- Server Configuration
- Automatic IP Address Assignment
- Name Resolution
- Cisco IOS Verification
- Network Troubleshooting

---

## 🎯 Outcome

Successfully configured DHCP and DNS services allowing client devices to automatically obtain network settings and resolve hostnames across the local network.