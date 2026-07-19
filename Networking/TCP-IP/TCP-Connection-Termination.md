# TCP Connection Termination

## What is TCP Connection Termination?

TCP Connection Termination is the process of gracefully closing a TCP connection after data transfer is complete.

It is commonly called the Four-Way Handshake.

---

# Steps

| Step | Packet | Purpose |
|------|--------|---------|
| 1 | FIN | Client requests to close the connection |
| 2 | ACK | Server acknowledges the request |
| 3 | FIN | Server requests to close its side |
| 4 | ACK | Client acknowledges the request |

---

# Communication Flow

```text
Client
   │
   │ FIN
   ▼
Server
   │
   │ ACK
   ▼
Client
   │
   │ FIN
   ▼
Server
   │
   │ ACK
   ▼
Connection Closed
```

---

# Why Four Packets?

- TCP is a full-duplex protocol.
- Both client and server close their side of the connection independently.
- Each FIN must be acknowledged.

---

# What I Learned

- TCP uses a Four-Way Handshake to close a connection.
- Connection termination starts with a FIN packet.
- Every FIN is acknowledged with an ACK.
- Both client and server close their communication independently.
- A TCP connection is fully closed only after the final ACK.

---

# Wireshark

✅ Can be seen in Wireshark.

Display Filter:

```text
tcp.flags.fin == 1
```

Observe packets such as:

```text
Client → Server : FIN, ACK
Server → Client : ACK
Server → Client : FIN, ACK
Client → Server : ACK
```
