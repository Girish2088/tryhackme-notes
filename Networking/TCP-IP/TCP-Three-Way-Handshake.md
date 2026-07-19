# TCP Three-Way Handshake

## What is the Three-Way Handshake?

The TCP Three-Way Handshake is the process used to establish a reliable connection between a client and a server before data transfer begins.

---

# Steps

| Step | Packet | Purpose |
|------|--------|---------|
| 1 | SYN | Client requests a connection |
| 2 | SYN + ACK | Server accepts the request |
| 3 | ACK | Client confirms the connection |

---

# Communication Flow

```text
Client
   │
   │ SYN
   ▼
Server
   │
   │ SYN-ACK
   ▼
Client
   │
   │ ACK
   ▼
Connection Established
```

---

# Why is it Needed?

- Ensures both client and server are ready.
- Establishes a reliable TCP connection.
- Synchronizes sequence numbers before data transfer.

---

# What I Learned

- TCP uses a Three-Way Handshake before sending data.
- The handshake consists of SYN, SYN-ACK, and ACK packets.
- Data transfer begins only after the connection is established.
- Sequence numbers are synchronized during the handshake.
- Every TCP connection starts with a Three-Way Handshake.

---

# Wireshark

✅ Can be seen in Wireshark.

Display Filter:

```text
tcp.flags.syn == 1 || tcp.flags.ack == 1
```

Observe:

```text
Client → Server : SYN
Server → Client : SYN, ACK
Client → Server : ACK
```
