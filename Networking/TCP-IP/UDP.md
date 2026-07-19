# UDP (User Datagram Protocol)

## What is UDP?

UDP is a connectionless transport protocol that sends data without establishing a connection and without guaranteeing delivery.

It focuses on speed and low overhead.

---

# Key Characteristics

| Feature | Description |
|---|---|
| Connection | No connection setup |
| Reliability | No guarantee of delivery |
| Order | No guarantee of order |
| Speed | Very fast |
| Overhead | Very low |

---

# Communication Flow

```text
Client ─────► Server
```

No handshake.

No acknowledgements.

No retransmissions.

---

# Common Use Cases

| Application | Reason |
|---|---|
| DNS | Small request/response |
| Video Streaming | Speed more important than reliability |
| Voice Calls (VoIP) | Low latency required |
| Online Gaming | Fast communication needed |
| Live Broadcasting | Continuous data flow |

---

# UDP Header

| Field | Purpose |
|---|---|
| Source Port | Sender application |
| Destination Port | Receiver application |
| Length | Total UDP packet size |
| Checksum | Error detection |

---

# What I Learned

- UDP is a connectionless protocol.
- It sends data without establishing a connection.
- It does not use acknowledgements (ACKs).
- It does not retransmit lost packets.
- It is faster than TCP because it has less overhead.
- Applications such as DNS, streaming, gaming, and VoIP commonly use UDP.

---

# Wireshark

✅ Can be seen in Wireshark.

Use the display filter:

```text
udp
```

Expand the **User Datagram Protocol** section to observe:

```text
Source Port
Destination Port
Length
Checksum
```

Example:

```text
Source Port: 40941
Destination Port: 443 (DNS)
```
