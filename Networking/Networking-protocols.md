

# HTTP = Web Pages

### Purpose

Used to communicate with web servers and load websites.

### Common Methods

| Method | Use                |
| ------ | ------------------ |
| GET    | Retrieve data      |
| POST   | Send data          |
| PUT    | Create/Update data |
| DELETE | Remove data        |

### Example

```http
GET / HTTP/1.1
Host: example.com
```

### Practical Tools

```bash
curl http://site.com
```

```bash
telnet IP 80
```

```bash
nc IP 80
```

### Memory Hook

```text
HTTP = Read and Send Web Data
```

---

# HTTPS = Secure HTTP

### Purpose

Same as HTTP but encrypted using TLS/SSL.

### Default Port

```text
443
```

### Practical Tool

```bash
curl https://site.com
```

### Memory Hook

```text
HTTPS = Secure Web Traffic
```

---

# FTP = File Transfer

### Purpose

Upload and download files.

### Default Port

```text
21
```

### Connect

```bash
ftp IP
```

### Important Commands

| Command    | Purpose       |
| ---------- | ------------- |
| USER       | Username      |
| PASS       | Password      |
| ls / LIST  | View files    |
| get / RETR | Download file |
| put / STOR | Upload file   |
| quit       | Exit          |

### Memory Hook

```text
FTP = Transfer Files
```

---

# SMTP = Send Email

### Purpose

Send email to mail servers.

### Default Port

```text
25
```

### Connect

```bash
telnet IP 25
```

### Important Commands

| Command     | Purpose       |
| ----------- | ------------- |
| HELO / EHLO | Start session |
| MAIL FROM   | Sender        |
| RCPT TO     | Recipient     |
| DATA        | Write email   |
| QUIT        | Exit          |

### Memory Hook

```text
SMTP = Send Mail
```

---

# POP3 = Download Email

### Purpose

Download emails from server.

### Default Port

```text
110
```

### Connect

```bash
telnet IP 110
```

### Important Commands

| Command | Purpose      |
| ------- | ------------ |
| USER    | Username     |
| PASS    | Password     |
| LIST    | Show emails  |
| RETR    | Read email   |
| DELE    | Delete email |
| QUIT    | Exit         |

### Memory Hook

```text
POP3 = Download Mail
```

---

# IMAP = Sync Email

### Purpose

Read emails while keeping them synchronized across devices.

### Default Port

```text
143
```

### Connect

```bash
telnet IP 143
```

### Important Commands

| Command | Purpose      |
| ------- | ------------ |
| LOGIN   | Authenticate |
| SELECT  | Open mailbox |
| FETCH   | Read email   |
| COPY    | Copy email   |
| MOVE    | Move email   |
| LOGOUT  | Exit         |

### Memory Hook

```text
IMAP = Sync Mail
```

---

# Telnet = Manual TCP Client

### Purpose

Connect directly to TCP services and interact manually.

### Syntax

```bash
telnet IP PORT
```

### Examples

```bash
telnet IP 80
telnet IP 25
telnet IP 110
telnet IP 143
```

### Uses

* Check if service is running
* Banner grabbing
* Manual protocol testing
* CTFs and TryHackMe labs

### Memory Hook

```text
Telnet = Manual TCP Connection
```

---

# One-Line Revision

```text
HTTP  = Web Pages

HTTPS = Secure Web

FTP   = File Transfer

SMTP  = Send Mail

POP3  = Download Mail

IMAP  = Sync Mail

Telnet = Manual TCP Connection
```

---

# Port Revision

```text
HTTP   → 80

HTTPS  → 443

FTP    → 21

SMTP   → 25

POP3   → 110

IMAP   → 143
```

---

# Email Flow

```text
SMTP
 ↓
Mail Server
 ↓
POP3 / IMAP
 ↓
User Reads Email
```
