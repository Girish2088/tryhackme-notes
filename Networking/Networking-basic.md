## DHCP = Get IP

### Purpose

Automatically provides:

* IP Address
* Subnet Mask
* Gateway
* DNS Server

### Example

```text
Connect to WiFi
      ↓
DHCP assigns settings
      ↓
Internet works
```

### Memory Hook

```text
DHCP = Automatic Network Setup
```

---

## ARP = Get MAC

### Purpose

```text
IP Address → MAC Address
```

### Example

```text
Know Router IP:
192.168.1.1

Need Router MAC

ARP:
"Who has 192.168.1.1?"

Router:
"My MAC is XX:XX:XX:XX:XX:XX"
```

### Memory Hook

```text
Know IP
Need MAC
Use ARP
```

---

## DNS = Name → IP

### Purpose

```text
Domain Name → IP Address
```

### Example

```text
youtube.com
      ↓
142.250.x.x
```

### Memory Hook

```text
DNS = Internet Phonebook
```

---

## ICMP = Diagnostics

### Purpose

* Connectivity Testing
* Error Reporting
* Troubleshooting

### Example

```bash
ping google.com
```

```text
Are you alive?
      ↓
Yes
```

### Memory Hook

```text
ICMP = Network Health Check
```

---

## Traceroute = Find Route

### Purpose

```text
Shows every router
between source and destination
```

### Example

```text
My Router
     ↓
ISP Router
     ↓
Regional Router
     ↓
Google Router
```

### Memory Hook

```text
Traceroute = GPS of a Packet
```
Example:
```
traceroute google.com
```
Windows
```
tracert <destination>
```
Example:
```
tracert google.com
```
Common Options (Linux)

Disable DNS resolution:
```
traceroute -n google.com
```
Limit the maximum number of hops:
```
traceroute -m 10 google.com
```
Use ICMP packets:
```
traceroute -I google.com
```
---

## Routing = Choose Path

### Purpose

```text
Determine the best path
for packets to travel
```

### Example

```text
India
  ↓
USA

Multiple routes exist

Router chooses the best one
```

### Memory Hook

```text
Routing = Packet Navigation System
```

---

## NAT = Private ↔ Public

### Purpose

```text
Private IP ↔ Public IP
```

### Example

```text
192.168.1.10
      ↓
49.x.x.x
```

Router translates private addresses before sending traffic to the Internet.

### Memory Hook

```text
NAT = Internet Translator
```

---

## WHOIS = Domain Owner

### Purpose

Shows information about a registered domain.

### Example

```bash
whois example.com
```

May reveal:

```text
Owner
Registrar
Creation Date
Expiry Date
```

### Memory Hook

```text
WHOIS = Domain Registration Information
```

---

# One-Line Revision

```text
DHCP       → Assigns Network Configuration

ARP        → Finds MAC Address

DNS        → Converts Name → IP

ICMP       → Diagnostics & Connectivity

Traceroute → Shows Packet Path

Routing    → Chooses Best Path

NAT        → Private IP ↔ Public IP

WHOIS      → Domain Registration Info
```

---

# Website Journey

```text
Connect to Network
      ↓
DHCP
      ↓
DNS
      ↓
ARP
      ↓
NAT
      ↓
Routing
      ↓
Web Server
      ↓
Response
```

### Simple Flow

```text
DHCP = Get IP

DNS = Get Server IP

ARP = Get Router MAC

NAT = Reach Internet

Routing = Find Path

Website Loads
```

