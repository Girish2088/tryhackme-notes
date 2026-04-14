


## ✍️ Text Editors

* `nano filename`

  * Simple, beginner-friendly terminal editor

* `vim filename`

  * Advanced editor with powerful features (steeper learning curve)

---

## 📥 File Downloading & Transfer

### 🌐 `wget` (Download from Web)

Used to download files from a **web server (HTTP/HTTPS/FTP)**.

**Syntax:**

```bash
wget <URL>
```

**Example:**

```bash
wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt
```

✅ Key Points:

* Works with URLs only
* Does NOT use `username@ip`
* Used for downloading from websites, not PCs directly

---

### 🔐 `scp` (Secure Copy over SSH)

Used to transfer files between **local machine ↔ remote machine**.

📌 Rule:
**Command runs from the machine you are currently using**

---

#### 📤 Local → Remote

```bash
scp localfile.txt username@remoteIP:/path/on/remote/
```

**Example:**

```bash
scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt
```

---

#### 📥 Remote → Local

```bash
scp username@remoteIP:/path/on/remote/file.txt localfile.txt
```

**Example:**

```bash
scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt
```

---

### 🧠 Mental Model

* Left = **source**
* Right = **destination**

---

## 🌐 Temporary File Sharing (Python HTTP Server)

Convert a remote machine into a **simple web server**.

### Steps:

1. SSH into remote machine:

```bash
ssh username@remoteIP
```

2. Start server:

```bash
python3 -m http.server 8000
```

3. From your local machine:

```bash
wget http://remoteIP:8000/filename
```

---

### ⚠️ Notes:

* Serves files from **current directory**
* No authentication (not secure)
* Port `8000` must be open
* Useful for quick file sharing

---

## ⚙️ Process Management

### 🔍 View Processes

* `ps` → show current processes
* `ps aux` → detailed list of all processes
* `ps <PID>` → info about specific process
* `top` → real-time process monitoring

---

### ❌ Kill Processes

```bash
kill <PID>
```

⚠️ Your note said “kill all process” — wrong.
That would be system suicide.

---

### 🔥 Signals

* `SIGTERM` → graceful stop (default)
* `SIGKILL` → force kill (no cleanup)
* `SIGSTOP` → pause process

Example:

```bash
kill -9 <PID>   # SIGKILL
```

---

## 🧩 Service Management (`systemctl`)

Used to manage services via `systemd`.

**Syntax:**

```bash
systemctl <option> <service>
```

### Common Commands:

* `start` → start service
* `stop` → stop service
* `enable` → start at boot
* `disable` → disable at boot
* `status` → check status

**Example:**

```bash
systemctl start apache2
```

---

## 🧠 Job Control

* `Ctrl + Z` → pause process (send to background)
* `fg` → bring process to foreground

---

## 📦 Package Management

* `apt` → package manager (install/remove software)
* `repo` → source of software packages
* `GPG key` → verifies package authenticity

---

## ⚡ Key Takeaways (so you stop mixing tools again)

* `scp` → machine-to-machine (uses SSH, needs username@ip)
* `wget` → download from web (uses URL only)
* `python3 -m http.server` → turns PC into temporary web server

