# Ports

## What is a Port?

A Port is a logical number used to identify a specific application or service running on a device.

An IP Address identifies the device, while a Port identifies the application.

---

# IP vs Port

| IP Address | Port |
|------------|------|
| Identifies a device | Identifies an application/service |
| Example: 192.168.1.10 | Example: 80 (HTTP) |

---

# Common Ports

| Port | Service |
|------|---------|
| 20/21 | FTP |
| 22 | SSH |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 443 | HTTPS |

---

# Port Ranges

| Range | Type |
|-------|------|
| 0 - 1023 | Well Known Ports |
| 1024 - 49151 | Registered Ports |
| 49152 - 65535 | Dynamic / Ephemeral Ports |

---

# Communication Example

```text
Browser
        ↓
Destination IP = 142.xx.xx.xx
        ↓
Destination Port = 443
        ↓
HTTPS Service
```

---

# What I Learned

- IP Address identifies the destination device.
- Port identifies the destination application or service.
- Multiple applications can run on the same device using different ports.
- TCP and UDP both use Port Numbers.
- Source Ports are usually temporary (ephemeral).
- Destination Ports identify well-known services like HTTP, HTTPS, DNS, and SSH.

---

```
