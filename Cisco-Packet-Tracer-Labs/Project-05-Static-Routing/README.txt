# Project 5 - Static Routing

## Objective

Configure static routing between two routers to enable communication between different LANs using Cisco Packet Tracer.

---

## Network Topology

![Topology](topology.png)

---

## Devices Used

- 2 × Cisco 2911 Routers
- 2 × Cisco 2960 Switches
- 4 × PCs

---

## IP Addressing

| Device | IP Address |
|---------|------------|
| Router1 G0/0 | 192.168.10.1/24 |
| Router1 G0/1 | 10.10.10.1/30 |
| Router2 G0/0 | 192.168.20.1/24 |
| Router2 G0/1 | 10.10.10.2/30 |

---

## Configuration

### Router 1

- Configured LAN and WAN interfaces
- Added static route to 192.168.20.0/24

### Router 2

- Configured LAN and WAN interfaces
- Added static route to 192.168.10.0/24

---

## Verification

From PC0

```cmd
ping 192.168.20.10
```

Expected Result

```text
Reply from 192.168.20.10
```

Verify routing table

```bash
show ip route
```

---

## Skills Learned

- Static Routing
- Cisco IOS CLI
- IPv4 Addressing
- Router Configuration
- Routing Verification
- Network Troubleshooting

---

## Outcome

Successfully established communication between two different LANs using static routing and verified end-to-end connectivity.