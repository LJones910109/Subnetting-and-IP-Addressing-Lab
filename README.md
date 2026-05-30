# 🔢 Subnetting and IP Addressing Lab

## Objective
Demonstrate understanding of IPv4 and IPv6 subnetting, CIDR notation, 
and IP addressing concepts used in network design and troubleshooting.

---

## 🛠️ Tools Used
- Windows 11 Calculator
- Command Prompt (ipconfig, ping)
- Subnet calculators for verification
- DeVry University Networking Coursework

---

## 📋 IPv4 Addressing Fundamentals

### IP Address Classes
| Class | Range | Default Subnet Mask | Use |
|---|---|---|---|
| A | 1.0.0.0 - 126.255.255.255 | 255.0.0.0 | Large networks |
| B | 128.0.0.0 - 191.255.255.255 | 255.255.0.0 | Medium networks |
| C | 192.0.0.0 - 223.255.255.255 | 255.255.255.0 | Small networks |

### Private IP Ranges
| Range | CIDR | Use |
|---|---|---|
| 10.0.0.0 - 10.255.255.255 | 10.0.0.0/8 | Large private networks |
| 172.16.0.0 - 172.31.255.255 | 172.16.0.0/12 | Medium private networks |
| 192.168.0.0 - 192.168.255.255 | 192.168.0.0/16 | Home and small office |

---

## 🔢 Subnetting Practice

### Example 1 — Basic Subnet
Network: 192.168.1.0/24

| Field | Value |
|---|---|
| Network Address | 192.168.1.0 |
| Subnet Mask | 255.255.255.0 |
| First Host | 192.168.1.1 |
| Last Host | 192.168.1.254 |
| Broadcast | 192.168.1.255 |
| Total Hosts | 254 |

---

### Example 2 — Subnetting into Smaller Networks
Network: 192.168.1.0/26

| Field | Value |
|---|---|
| Network Address | 192.168.1.0 |
| Subnet Mask | 255.255.255.192 |
| First Host | 192.168.1.1 |
| Last Host | 192.168.1.62 |
| Broadcast | 192.168.1.63 |
| Total Hosts | 62 |
| Total Subnets | 4 |

---

### Example 3 — VLSM (Variable Length Subnet Masking)
Scenario: A company needs 3 subnets:
- Subnet A: 50 hosts
- Subnet B: 25 hosts
- Subnet C: 10 hosts

Starting network: 192.168.10.0/24

| Subnet | CIDR | Mask | Hosts Available |
|---|---|---|---|
| Subnet A | 192.168.10.0/26 | 255.255.255.192 | 62 |
| Subnet B | 192.168.10.64/27 | 255.255.255.224 | 30 |
| Subnet C | 192.168.10.96/28 | 255.255.255.240 | 14 |

---

## 🌐 IPv6 Addressing

### IPv6 vs IPv4 Comparison
| Feature | IPv4 | IPv6 |
|---|---|---|
| Address Length | 32 bits | 128 bits |
| Format | Decimal (192.168.1.1) | Hexadecimal (2001:db8::1) |
| Total Addresses | ~4.3 billion | 340 undecillion |
| Header Size | 20 bytes | 40 bytes |
| NAT Required | Yes | No |

### IPv6 Address Types
- Unicast — One to one communication
- Multicast — One to many communication
- Anycast — One to nearest communication

### Common IPv6 Prefixes
| Prefix | Use |
|---|---|
| 2000::/3 | Global unicast (public) |
| FC00::/7 | Unique local (private) |
| FE80::/10 | Link local |
| ::1/128 | Loopback |

---

## 🧮 Subnetting Quick Reference

### Powers of 2
| Power | Value | Hosts Available |
|---|---|---|
| /24 | 256 | 254 |
| /25 | 128 | 126 |
| /26 | 64 | 62 |
| /27 | 32 | 30 |
| /28 | 16 | 14 |
| /29 | 8 | 6 |
| /30 | 4 | 2 |

---

## 🧠 What I Learned
- How to calculate subnets, host ranges, and broadcast addresses
- How VLSM allows efficient use of IP address space
- The key differences between IPv4 and IPv6
- How subnetting applies to real network design scenarios

---

## 📚 Resources Used
- DeVry University Networking Coursework
- CompTIA Network+ Study Materials
- RFC 1918 (Private Address Space)
- RFC 4291 (IPv6 Addressing Architecture)
