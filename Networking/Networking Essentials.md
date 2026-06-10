# Networking Fundamentals - Quick Revision Notes

---

# DHCP (Dynamic Host Configuration Protocol)

### Purpose

Automatically provides:

* IP Address
* Subnet Mask
* Gateway
* DNS Server

### Ports

```text
DHCP Server = UDP 67
DHCP Client = UDP 68
```

### DORA Process

```text
D = Discover
O = Offer
R = Request
A = Acknowledge
```

### Flow

```text
Client → DHCP Discover
Server → DHCP Offer
Client → DHCP Request
Server → DHCP ACK
```

### Result

```text
IP Address Assigned
Gateway Assigned
DNS Assigned
```

---

# ARP (Address Resolution Protocol)

### Purpose

```text
IP Address → MAC Address
```

### Flow

```text
ARP Request
Who has X.X.X.X?

ARP Reply
X.X.X.X is at XX:XX:XX:XX:XX:XX
```

### Important

ARP Request:

```text
Destination MAC

FF:FF:FF:FF:FF:FF
(Broadcast)
```

### Result

```text
ARP Table Entry Created

IP ↔ MAC
```

---

# DNS (Domain Name System)

### Purpose

```text
Domain Name → IP Address
```

### Example

```text
google.com
     ↓
142.250.x.x
```

---

# ICMP (Internet Control Message Protocol)

### Purpose

* Diagnostics
* Error Reporting
* Network Troubleshooting

### Common Commands

```text
ping
traceroute
```

---

# Ping

### Uses

* Host Reachability
* Connectivity Testing
* RTT Measurement

### ICMP Types

```text
Echo Request = Type 8

Echo Reply = Type 0
```

### RTT

```text
Round Trip Time
```

### Example

```bash
ping 8.8.8.8 -c 4
```

---

# Traceroute

### Purpose

```text
Discover Route to Destination
```

### Uses

```text
TTL Field
```

### ICMP Type

```text
Time Exceeded = Type 11
```

### Process

```text
TTL = 1 → Router 1 Revealed

TTL = 2 → Router 2 Revealed

TTL = 3 → Router 3 Revealed
```

### Hop

```text
1 Router Crossed = 1 Hop
```

---

# Routing

### Purpose

```text
Determine Best Path
Between Source and Destination
```

### Router Uses

```text
Routing Table
```

### Decision Based On

```text
Destination IP
```

---

# Routing Protocols

## RIP

```text
Routing Information Protocol
```

Uses:

```text
Hop Count
```

Chooses:

```text
Lowest Number of Hops
```

---

## OSPF

```text
Open Shortest Path First
```

Uses:

```text
Network Topology
```

Chooses:

```text
Best / Shortest Path
```

---

## EIGRP

```text
Enhanced Interior Gateway Routing Protocol
```

Uses:

* Bandwidth
* Delay
* Reliability

Chooses:

```text
Most Efficient Route
```

---

## BGP

```text
Border Gateway Protocol
```

Purpose:

```text
Routing Between Large Networks
(ISPs, Google, Cloudflare, Amazon)
```

### Most Important

```text
Internet Runs Primarily On BGP
```

---

# NAT (Network Address Translation)

### Purpose

```text
Private IP ↔ Public IP Translation
```

### Why?

```text
IPv4 Address Conservation
```

### Example

```text
Private

192.168.1.10
192.168.1.11
192.168.1.12

        ↓

Public

49.36.120.50
```

### Router Maintains

```text
NAT Translation Table
```

### Translation Example

```text
192.168.1.10:15401
        ↓
49.36.120.50:30001
```

---

# NAT Connection Limit

### TCP Ports

```text
0 - 65535
```

### Approximate Connections

```text
≈ 64,000 Simultaneous TCP Connections
Per Public IP
```

(Assuming infinite CPU and memory)

---

# Private IPv4 Ranges

### Class A

```text
10.0.0.0
to
10.255.255.255
```

### Class B

```text
172.16.0.0
to
172.31.255.255
```

### Class C

```text
192.168.0.0
to
192.168.255.255
```

---

# ICMP Types to Remember

| Type | Meaning       |
| ---- | ------------- |
| 0    | Echo Reply    |
| 8    | Echo Request  |
| 11   | Time Exceeded |

---

# Ports to Remember

| Protocol    | Port   |
| ----------- | ------ |
| DHCP Server | UDP 67 |
| DHCP Client | UDP 68 |

---

# THM Exam Revision Sheet

```text
DHCP  → Assign IP

ARP   → IP to MAC

DNS   → Domain to IP

ICMP  → Diagnostics

Ping  → Echo Request/Reply

Traceroute → Uses TTL

Routing → Path Selection

RIP   → Lowest Hops

OSPF  → Best Path

EIGRP → Efficient Path

BGP   → Internet Routing

NAT   → Private ↔ Public IP
```

## Complete Packet Journey

```text
Connect Network
      ↓
DHCP
      ↓
ARP
      ↓
DNS
      ↓
Routing
      ↓
NAT
      ↓
Internet
      ↓
Destination
      ↓
Response
```
