# TCP (Transmission Control Protocol)

## What is TCP?

TCP (Transmission Control Protocol) is a connection-oriented transport protocol that provides reliable, ordered, and error-checked data delivery between devices.

---

# Features

| Feature | Description |
|---------|-------------|
| Connection | Connection-Oriented |
| Reliability | Reliable |
| Speed | Slower than UDP |
| Delivery | Ordered |
| Retransmission | Yes |
| ACK | Yes |

---

# Why TCP is Reliable?

- Uses Sequence Numbers to keep packets in order.
- Uses Acknowledgements (ACKs) to confirm delivery.
- Detects errors using Checksum.
- Retransmits lost or corrupted packets.

---

# Common Uses

- HTTP / HTTPS
- File Transfer (FTP)
- Email
- SSH

---

# Important TCP Header Fields

| Field | Purpose |
|--------|---------|
| Source Port | Sender application |
| Destination Port | Receiver application |
| Sequence Number | Packet ordering |
| Acknowledgement Number | Confirms received data |
| Flags | SYN, ACK, FIN, RST |
| Window Size | Flow control |
| Checksum | Error detection |

---

# Communication Flow

```text
Connection Established
        ↓
Data Sent
        ↓
ACK Received
        ↓
Retransmit if Required
        ↓
Connection Closed
```

---

# What I Learned

- TCP is a connection-oriented protocol.
- TCP provides reliable and ordered communication.
- TCP uses Sequence Numbers to maintain packet order.
- TCP uses ACKs to confirm successful delivery.
- TCP retransmits lost or corrupted packets.
- TCP uses Checksum to detect transmission errors.
- TCP is commonly used for web browsing, file transfers, emails, and SSH.

---

# Wireshark

✅ Can be seen in Wireshark.

Display Filter:

```text
tcp
```

Expand:

```text
Transmission Control Protocol
```

Observe:

- Source Port
- Destination Port
- Sequence Number
- Acknowledgement Number
- Flags
- Window Size
- Checksum
