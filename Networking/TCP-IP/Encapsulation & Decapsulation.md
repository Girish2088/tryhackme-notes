# Encapsulation & Decapsulation

## What is Encapsulation?

Encapsulation is the process of adding protocol headers as data moves down the TCP/IP stack before transmission.

Each layer adds its own header to the data.

---

# Sending Process (Encapsulation)

```text
Application Data
        ↓
TCP Header Added
        ↓
IP Header Added
        ↓
Ethernet Header Added
        ↓
Frame Sent through NIC
```

---

# Receiving Process (Decapsulation)

```text
Frame Received
        ↓
Ethernet Header Removed
        ↓
IP Header Removed
        ↓
TCP Header Removed
        ↓
Application Receives Data
```

---

# Why Encapsulation?

- Every layer has a specific responsibility.
- Each layer adds its own information (Header).
- Headers help deliver the data correctly.

---

# What I Learned

- Encapsulation means adding headers while sending data.
- Decapsulation means removing headers while receiving data.
- TCP adds the Transport Layer header.
- IP adds the Network Layer header.
- Ethernet adds the Data Link Layer header.
- The final Frame is transmitted through the NIC.
- Wireshark shows every protocol header separately.

---

# Wireshark

✅ Can be seen in Wireshark.

Expand any HTTP packet:

```text
Frame
    ↓
Ethernet II
    ↓
IPv4
    ↓
TCP
    ↓
HTTP
```

This is encapsulation visualized.
