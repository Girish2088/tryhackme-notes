# TCP Connection Termination

## What is TCP Connection Termination?

TCP Connection Termination is the process of gracefully closing a TCP connection after data transfer is complete.

It is commonly called the **Four-Way Handshake**.

---

# Steps

| Step | Packet | Purpose |
|------|--------|---------|
| 1 | FIN | Client requests to close the connection |
| 2 | ACK | Server acknowledges the request |
| 3 | FIN | Server requests to close its side |
| 4 | ACK | Client acknowledges the request |

---

# Theoretical Communication Flow

```text
Client                          Server
  │                               │
  │ -------- FIN ------------->   │
  │                               │
  │ <------- ACK -------------    │
  │                               │
  │ <------- FIN -------------    │
  │                               │
  │ -------- ACK ------------->   │
  │                               │
Connection Closed
```

---

# Why Four Packets?

- TCP is a full-duplex protocol.
- Client and Server close their side of the connection independently.
- Every FIN must be acknowledged with an ACK.

---

# What I Learned

- TCP uses a Four-Way Handshake to terminate a connection.
- The connection is closed gracefully after data transfer is complete.
- Both client and server independently close their side of the connection.
- Every FIN is acknowledged with an ACK before the connection is fully closed.

---

# Wireshark

✅ Can be seen in Wireshark.

Display Filter:

```text
tcp.flags.fin == 1
```

In real packet captures, you'll usually see:

```text
Client → Server : FIN, ACK
Server → Client : ACK
Server → Client : FIN, ACK
Client → Server : ACK
```

---

# Note

The theoretical Four-Way Handshake is:

```text
FIN
↓
ACK
↓
FIN
↓
ACK
```

However, in real TCP implementations, the **FIN** and **ACK** flags are often combined into a single packet (`FIN, ACK`) to reduce overhead.

So, in Wireshark, you'll commonly observe:

```text
FIN, ACK
↓
ACK
↓
FIN, ACK
↓
ACK
```
