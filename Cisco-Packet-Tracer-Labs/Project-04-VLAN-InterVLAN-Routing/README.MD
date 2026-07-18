# Project 4 - VLAN and Inter-VLAN Routing

## 📌 Objective

Configure VLANs on a Cisco switch and enable communication between different VLANs using Router-on-a-Stick (Inter-VLAN Routing).

---

## 🖥 Network Topology

![Topology](topology.png)

---

## 🛠 Devices Used

- Cisco 1941 Router
- Cisco 2960 Switch
- 6 PCs

---

## 🌐 VLAN Configuration

| VLAN ID | Name | Devices |
|----------|------|---------|
| 10 | HR | PC0, PC1 |
| 20 | SALES | PC2, PC3 |
| 30 | IT | PC4, PC5 |

---

## 🌐 IP Addressing

### VLAN 10 (HR)

Gateway

192.168.10.1

PC0

192.168.10.10

PC1

192.168.10.11

---

### VLAN 20 (SALES)

Gateway

192.168.20.1

PC2

192.168.20.10

PC3

192.168.20.11

---

### VLAN 30 (IT)

Gateway

192.168.30.1

PC4

192.168.30.10

PC5

192.168.30.11

---

## ⚙ Switch Configuration

Configured:

- VLAN 10
- VLAN 20
- VLAN 30
- Access Ports
- Trunk Port

---

## ⚙ Router Configuration

Configured Router-on-a-Stick using subinterfaces:

- G0/0.10
- G0/0.20
- G0/0.30

Each subinterface was configured with:

- 802.1Q encapsulation
- IPv4 address
- Default gateway for each VLAN

---

## 🔍 Verification

Switch Commands

```bash
show vlan brief

show interfaces trunk

show mac address-table
```

Router Commands

```bash
show ip interface brief

show running-config
```

PC Commands

```cmd
ping

ipconfig
```

---

## ✅ Test Results

- VLANs created successfully
- Trunk link operational
- Inter-VLAN communication successful
- All PCs successfully reached devices in other VLANs

---

## 📚 Skills Learned

- VLAN Configuration
- VLAN Port Assignment
- Trunk Configuration
- Router-on-a-Stick
- Inter-VLAN Routing
- Cisco IOS CLI
- Network Troubleshooting

---

## 🎯 Outcome

Successfully implemented VLAN segmentation and Inter-VLAN Routing using Router-on-a-Stick, enabling secure communication between multiple departments on different VLANs.