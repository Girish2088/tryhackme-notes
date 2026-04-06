

## Key Concepts Learned

- OSI Model (7 Layers)
- TCP/IP Model (4 Layers)
- Packet vs Frame
- TCP vs UDP communication
- Ports and networking basics
- Firewalls and VPNs
- Encapsulation and data flow

---

## 🌐 OSI Model (7 Layers)

1. **Physical**
   - Hardware components (cables, NIC)
   - Example: Ethernet cable

2. **Data Link**
   - Uses MAC addresses
   - Handles physical addressing
   - Device: NIC

3. **Network**
   - Handles routing using IP addresses
   - Protocols: OSPF, RIP
   - Device: Router

4. **Transport**
   - Handles data transmission using:
     - TCP (reliable)
     - UDP (fast)

5. **Session**
   - Manages connection between devices

6. **Presentation**
   - Handles encryption (e.g., HTTPS)

7. **Application**
   - User interaction layer (GUI, apps, protocols)

---

## 📦 Packet vs Frame

- **Packet** → Contains IP address (Layer 3)
- **Frame** → Data at Data Link layer (MAC level)

---

## 🔄 Encapsulation

- Data moves down OSI layers → headers added  
- Receiver removes headers → decapsulation  

---

## ⚙️ TCP vs UDP

### 🔐 TCP (Reliable)
- Connection-based (3-way handshake)
- Ensures order and delivery
- Slower but accurate

**Use Cases:**
- Web browsing
- File transfer
- Email

---

### ⚡ UDP (Fast)
- Connectionless
- No delivery guarantee
- No order checking

**Use Cases:**
- Streaming
- Gaming
- Voice calls

---

## 🤝 TCP 3-Way Handshake

1. SYN → Client requests connection  
2. SYN-ACK → Server responds  
3. ACK → Client confirms  

➡ Connection established  

---

## 🔁 TCP Reliability Features

- Sequence numbers → order data  
- ACKs → confirm delivery  
- Checksum → detect errors  
- Retransmission → resend lost data  

---

## 🚀 TCP/IP Model (4 Layers)

1. Application  
2. Transport  
3. Internet  
4. Network Interface  

---

## 🔌 Ports

- Range: **0 – 65535**
- **0–1024** → Well-known ports  

Examples:
- 80 → HTTP  
- 443 → HTTPS  

---

## 🔀 Port Forwarding

- Allows external access to internal services  
- Configured on routers  
- Used for hosting services (e.g., web servers)

---

## 🔥 Firewalls

- Control incoming and outgoing traffic  
- Perform packet inspection  

### Types:
- **Stateful** → Tracks entire connection  
- **Stateless** → Inspects individual packets  

---

## 🔐 VPN (Virtual Private Network)

- Creates secure tunnel over the internet  
- Connects remote networks securely  
- Provides privacy and encryption  

### Technologies:
- PPP → Authentication & encryption  
- PPTP → Allows data transfer over network  
- IPsec → Encrypts IP communication  

