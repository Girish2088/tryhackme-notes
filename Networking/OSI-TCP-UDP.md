

# 🌐 OSI Model & Networking Notes

---

## 📚 OSI Model Overview

The OSI model provides a framework dictating how all networked devices send, receive, and interpret data.

---

## 🧱 OSI Layers (7 Layers)

| Layer No. | Layer Name   | Description                                                                     |
| --------- | ------------ | ------------------------------------------------------------------------------- |
| 1         | Physical     | the physical components of the hardware used in networking (ex: Ethernet cable) |
| 2         | Data Link    | physical addressing using MAC address via NIC                                   |
| 3         | Network      | routing and logical addressing using IP                                         |
| 4         | Transport    | data transfer using TCP and UDP                                                 |
| 5         | Session      | establishes and manages sessions                                                |
| 6         | Presentation | encryption and data formatting                                                  |
| 7         | Application  | user interaction via GUI and protocols                                          |

---

## 🔍 Layer Breakdown

### 1. Physical

* the physical components of the hardware used in networking
* ex: Ethernet cable

---

### 2. Data Link

* the physical addressing of the transmission
* it sends packet containing info of host computer(ip address) and add that in mac address of receiving computer
* Network Interface Card (NIC) provides unique MAC address

---

### 3. Network

* routing determines the most optimal path
* uses protocols:

  * OSPF (Open Shortest Path First)
  * RIP (Routing Information Protocol)
* routers = Layer 3 devices

---

### 4. Transport

| Protocol | Behavior                             |
| -------- | ------------------------------------ |
| TCP      | reliable, ordered, complete delivery |
| UDP      | fast, no guarantee, unordered        |

#### 📦 Example: Cat Image (4 chunks)

| Protocol | Result                                  |
| -------- | --------------------------------------- |
| TCP      | shows image only if all chunks received |
| UDP      | shows whatever chunks are received      |

---

### 5. Session

* When a connection is established, a session is created

---

### 6. Presentation

* encryption (example: HTTPS)

---

### 7. Application

* user interaction via GUI
* defines how data is accessed

---

# 📦 Packets vs Frames

| Term   | Meaning                           |
| ------ | --------------------------------- |
| Packet | contains IP address               |
| Frame  | encapsulated structure without IP |

📌 Analogy:

* Envelope = Frame
* Letter = Packet

---

# 🔗 TCP (Transmission Control Protocol)

| Feature     | Description                          |
| ----------- | ------------------------------------ |
| Reliability | Ensures correct and ordered delivery |
| Speed       | Slower than UDP                      |
| Usage       | file sharing, browsing, email        |

---

## ⚙️ TCP/IP Model (4 Layers)

| Layer             | Function          |
| ----------------- | ----------------- |
| Application       | HTTP, FTP         |
| Transport         | TCP, ports        |
| Internet          | IP addressing     |
| Network Interface | physical transfer |

---

## 📦 Encapsulation

* Data moves down layers → headers added
* Receiver removes headers → decapsulation

---

## ✅ Why TCP is Reliable

* Sequence numbers
* ACK (acknowledgement)
* Checksum
* Retransmission

---

## 🧾 TCP Headers

| Field                  | Purpose            |
| ---------------------- | ------------------ |
| Source Port            | sender port        |
| Destination Port       | service port       |
| Source IP              | sender address     |
| Destination IP         | receiver address   |
| Sequence Number        | order tracking     |
| Acknowledgement Number | confirms data      |
| Checksum               | integrity          |
| Flags                  | SYN, ACK, FIN, RST |
| Data                   | payload            |

---

## 🤝 Three-Way Handshake

| Step | Action  |
| ---- | ------- |
| 1    | SYN     |
| 2    | SYN-ACK |
| 3    | ACK     |

➡ Connection established

---

## 🔄 Data Flow

* send → ACK → resend if missing

---

## ❌ Connection Close

| Step | Action |
| ---- | ------ |
| 1    | FIN    |
| 2    | ACK    |
| 3    | FIN    |
| 4    | ACK    |

Flow:
`SYN → SYN-ACK → ACK → DATA → FIN → ACK`

---

# 🚀 UDP (User Datagram Protocol)

## 📌 Core Characteristics

| Feature     | Description    |
| ----------- | -------------- |
| Type        | Connectionless |
| Reliability | None           |
| Speed       | Very fast      |

---

## ⚙️ Behavior

* Stateless
* No ACK
* No retry

---

## 🎯 Use Cases

* Video streaming
* Voice calls
* Online gaming
* Live broadcast

---

## ⚡ Advantages

* Fast
* Low overhead
* Works on unstable networks

---

## ⚠️ Disadvantages

* No guarantee
* No order
* No recovery

---

## 🧾 UDP Headers

| Field            | Purpose  |
| ---------------- | -------- |
| Source IP        | sender   |
| Destination IP   | receiver |
| Source Port      | random   |
| Destination Port | fixed    |
| TTL              | lifetime |
| Data             | payload  |

---

## 🔄 UDP Flow

* send → maybe received → no response

---

## 🧠 Memory Hook

* **TCP:** Connect → Check → Deliver → Confirm
* **UDP:** Send → Hope → Done

---

# 🔢 PORT 101

| Range   | Meaning      |
| ------- | ------------ |
| 0–1024  | common ports |
| 0–65535 | total ports  |

Reference: [https://www.vmaxx.net/techinfo/ports.htm](https://www.vmaxx.net/techinfo/ports.htm)

---

# 🔀 Port Forwarding

* connects internal services to internet
* required for web servers
* configured on router

---

# 🔥 Firewall

A firewall controls incoming and outgoing traffic using packet inspection.

| Type      | Behavior                    |
| --------- | --------------------------- |
| Stateful  | analyzes full connection    |
| Stateless | analyzes individual packets |

---

# 🔐 VPN (Virtual Private Network)

* creates secure tunnel over internet
* connects different networks
* provides privacy

---

## 🛠️ VPN Technologies

| Technology | Function                             |
| ---------- | ------------------------------------ |
| PPP        | authentication + encryption          |
| PPTP       | allows PPP to travel outside network |
| IPSec      | encrypts using IP framework          |

---

