# TCP/IP Model

## What is TCP/IP?

TCP/IP (Transmission Control Protocol / Internet Protocol) is the networking model used on the Internet for communication between devices.

Unlike the OSI model (7 layers), the TCP/IP model has only 4 layers.

---

# TCP/IP Layers

| Layer | Purpose |
|--------|---------|
| Application | User applications and protocols (HTTP, FTP, DNS) |
| Transport | Reliable or fast communication using TCP or UDP |
| Internet | Routing using IP addresses |
| Network Interface | Transfers data using MAC addresses and physical media |

---

# OSI vs TCP/IP

| TCP/IP | OSI |
|---------|-----|
| Application | Application + Presentation + Session |
| Transport | Transport |
| Internet | Network |
| Network Interface | Data Link + Physical |

---

# Communication Flow

```text
Browser
    ↓
HTTP
    ↓
TCP
    ↓
IP
    ↓
Ethernet
    ↓
NIC
```

---

# What I Learned

- TCP/IP is the practical networking model used on the Internet.
- It has 4 layers.
- OSI is mainly used for learning and understanding networking concepts.
- TCP/IP is used by real-world networks and applications.
- Every network communication follows the TCP/IP model.
- Wireshark displays these layers in real network traffic.
