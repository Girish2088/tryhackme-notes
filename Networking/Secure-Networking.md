
# TLS = Encryption Layer

### Purpose

Protects:

* Confidentiality
* Integrity

Encrypts network traffic between client and server.

### Before TLS

```text
HTTP
SMTP
POP3
IMAP
```

Data travels in plaintext.

### After TLS

```text
Client
   ↓
TLS Encryption
   ↓
Server
```

Attackers see encrypted data instead of usernames, passwords, or messages.

### Certificates

Server proves identity using a:

```text
TLS Certificate
```

Issued by trusted:

```text
Certificate Authorities (CA)
```

Examples:

```text
Let's Encrypt
DigiCert
Sectigo
```

### Avoid

```text
Self-Signed Certificates
```

### Memory Hook

```text
TLS = Encryption Layer
```

---

# HTTPS = Secure Web

### Purpose

HTTP protected by TLS.

### Port

```text
443
```

### Flow

```text
DNS
 ↓
TCP Handshake
 ↓
TLS Handshake
 ↓
HTTP Communication
```

### Common Methods

```text
GET    → Retrieve Data

POST   → Send Data

PUT    → Create/Update

DELETE → Remove Data
```

### Memory Hook

```text
HTTPS = Secure Website Traffic
```

---

# SMTPS = Secure Email Sending

### Purpose

Send email securely using TLS.

### Ports

```text
465
587
```

### Important Commands

```text
HELO / EHLO

MAIL FROM

RCPT TO

DATA

QUIT
```

### Memory Hook

```text
SMTPS = Secure Send Mail
```

---

# POP3S = Secure Email Download

### Purpose

Download emails securely.

### Port

```text
995
```

### Characteristics

```text
Downloads mail

Often removes from server

Best for one device
```

### Important Commands

```text
USER

PASS

LIST

RETR

DELE

QUIT
```

### Memory Hook

```text
POP3S = Secure Download Mail
```

---

# IMAPS = Secure Email Sync

### Purpose

Synchronize emails securely across devices.

### Port

```text
993
```

### Characteristics

```text
Emails remain on server

Multiple devices stay synced
```

### Important Commands

```text
LOGIN

SELECT

FETCH

COPY

MOVE

LOGOUT
```

### Memory Hook

```text
IMAPS = Secure Mail Sync
```

---

# SSH = Secure Remote Login

### Purpose

Secure remote terminal access.

### Port

```text
22
```

### Replaces

```text
TELNET
```

### Command

```bash
ssh username@ip
```

Example:

```bash
ssh kali@10.10.10.10
```

### Features

```text
Encrypted Login

Public Key Authentication

Tunneling

File Transfer
```

### Memory Hook

```text
SSH = Secure Remote Access
```

---

# SFTP = Secure File Transfer

### Purpose

Transfer files securely using SSH.

### Port

```text
22
```

### Common Commands

```text
put = Upload

get = Download

ls  = List Files
```

### Flow

```text
Client
 ↓
SSH Tunnel
 ↓
Server
```

### Memory Hook

```text
SFTP = File Transfer over SSH
```

---

# FTPS = Secure FTP

### Purpose

FTP protected using TLS.

### Ports

```text
21 + TLS

or

990
```

### Difference

```text
FTP  = Plaintext

FTPS = Encrypted
```

### Memory Hook

```text
FTPS = FTP + TLS
```

---

# VPN = Virtual Private Network

### Purpose

Create a secure tunnel between networks.

### Flow

Without VPN:

```text
You
 ↓
Internet
```

With VPN:

```text
You
 ↓
Encrypted Tunnel
 ↓
VPN Server
 ↓
Internet / Private Network
```

### Uses

```text
Remote Work

Company Access

Home Lab Access

CCTV Access

TryHackMe

Hack The Box
```

### Types

#### Remote Access VPN

```text
One User
 ↓
Company Network
```

#### Site-to-Site VPN

```text
Branch Office
 ↓
Main Office
```

### Memory Hook

```text
VPN = Secure Tunnel
```

---

# Port Cheat Sheet

```text
HTTP    → 80

HTTPS   → 443

FTP     → 21

FTPS    → 21 / 990

SMTP    → 25

SMTPS   → 465 / 587

POP3    → 110

POP3S   → 995

IMAP    → 143

IMAPS   → 993

TELNET  → 23

SSH     → 22
```

---

# One-Line Revision

```text
TLS    → Encryption Layer

HTTPS  → Secure Web

SMTPS  → Secure Send Mail

POP3S  → Secure Download Mail

IMAPS  → Secure Mail Sync

SSH    → Secure Remote Login

SFTP   → Secure File Transfer via SSH

FTPS   → Secure FTP via TLS

VPN    → Secure Tunnel Between Networks
```

