

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
* Security feature such as data encryption (Like HTTPS when visiting a secure site) occur at this layer.

---

### 7. Application

* user interaction via GUI
* defines how data is accessed
* the layer in which protocols and rules are in place to determine how the user should interact with data sent or received.
* provide a friendly , Graphical User Interface (GUI) for users to interact with data sent or received.

---

# 📦 Packets vs Frames

| **Term**   | **Meaning**                                                                                                |
| ---------- | ---------------------------------------------------------------------------------------------------------- |
| **Packet** | Layer 3 (Network Layer) data. Contains Source IP and Destination IP.                                       |
| **Frame**  | Layer 2 (Data Link Layer) data. Contains Source MAC and Destination MAC, and carries the Packet inside it. |

---

## 📌 Analogy

* **Letter = Packet** (contains the destination IP information)
* **Envelope = Frame** (contains the MAC addresses and carries the packet)

---

## 🚀 Communication Flow

```text
Application Data
        ↓
Packet (Layer 3 - IP Address)
        ↓
Frame (Layer 2 - MAC Address + Packet)
        ↓
Sent through NIC
```

---
* **Packet belongs to Layer 3 (Network Layer).**
* **Frame belongs to Layer 2 (Data Link Layer).**
* **Packet contains IP addresses.**
* **Frame contains MAC addresses and carries the Packet.**
* **Packet travels from the source device to the final destination.**
* **Frame travels only to the next hop (Router/Gateway).**
* **At every router, the old Frame is removed and a new Frame is created with new Source and Destination MAC addresses.**
* **IP addresses usually remain the same during the journey, but MAC addresses change at every hop.**


