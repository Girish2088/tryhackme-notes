# TCP Connection Termination

## What is TCP Connection Termination?

TCP Connection Termination is the process of gracefully closing a TCP connection after data transfer is complete.

It is commonly known as the **Four-Way Handshake**.

---

## Why is it Needed?

Once the client and server finish exchanging data, both sides must properly close the connection.

Since TCP is **full-duplex**, each side closes its own half of the connection independently.

---

## Conceptual Process

TCP connection termination is commonly explained as:

```text
Client → Server : FIN
Server → Client : ACK
Server → Client : FIN
Client → Server : ACK
```

This is known as the **Four-Way Handshake** because each side independently closes its half of the connection.

---

## Practical Wireshark Capture

In real network captures, the ACK and FIN are often combined into a single packet when the receiving host is ready to close its connection immediately.

A common capture looks like:

```text
Client → Server : FIN, ACK
Server → Client : FIN, ACK
Client → Server : ACK
```

Although you may see only **three packets**, the TCP protocol still follows the same connection termination process. The server combines the ACK for the client's FIN with its own FIN into a single **FIN, ACK** packet.

---

## What I Learned

- TCP closes a connection gracefully after data transfer is complete.
- Connection termination is commonly explained as a Four-Way Handshake.
- Each side closes its own half of the connection independently.
- In real packet captures, **FIN** and **ACK** are often combined into a single **FIN, ACK** packet.
- Wireshark may show three packets instead of four due to this optimization.

---

## Wireshark

✅ Can be seen in Wireshark.

**Display Filter:**

```text
tcp.flags.fin == 1
```

Observe the TCP packets containing the **FIN** flag.

Common capture:

```text
Client → Server : FIN, ACK
Server → Client : FIN, ACK
Client → Server : ACK
```
