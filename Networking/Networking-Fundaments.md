## DHCP = Get IP

### Purpose

Automatically provides:

* IP Address
* Subnet Mask
* Gateway
* DNS Server

### Example

```text
Connect to WiFi
      ↓
DHCP assigns settings
      ↓
Internet works
```

### Memory Hook

```text
DHCP = Automatic Network Setup
```


# DORA Process

When a device joins a network, DHCP follows the **DORA** process to assign an IP address.

```
DHCP Discover
        ↓
DHCP Offer
        ↓
DHCP Request
        ↓
DHCP ACK (Acknowledge)
```

---

## Step 1 - DHCP Discover

**Who Sends:**
Client (Laptop / Mobile / PC)

**Purpose:**
Client bolta hai: **"Koi DHCP Server available hai?"**

---

## Step 2 - DHCP Offer

**Who Sends:**
DHCP Server

**Purpose:**
Server bolta hai: **"Haan, ye IP address le lo."**

---

## Step 3 - DHCP Request

**Who Sends:**
Client

**Purpose:**
Client bolta hai: **"Mujhe ye IP address chahiye."**

---

## Step 4 - DHCP ACK (Acknowledge)

**Who Sends:**
DHCP Server

**Purpose:**
Server bolta hai: **"Approved! Ab ye IP address tumhara hai."**

---

# Example

```
Laptop:
"Is there any DHCP Server?"

↓

DHCP Server:
"Take 192.168.1.25"

↓

Laptop:
"I want 192.168.1.25"

↓

DHCP Server:
"Approved. You can use it now."
```

---

# Easy Trick to Remember

**DORA = Discover → Offer → Request → Acknowledge**

* **Discover** → Client searches for DHCP Server.
* **Offer** → Server offers an IP address.
* **Request** → Client requests that IP.
* **ACK** → Server confirms and assigns the IP.

---

## ARP = Get MAC

### Purpose

```text
IP Address → MAC Address
```

### Example

```text
Know Router IP:
192.168.1.1

Need Router MAC

ARP:
"Who has 192.168.1.1?"

Router:
"My MAC is XX:XX:XX:XX:XX:XX"
```

### Memory Hook

```text
Know IP
Need MAC
Use ARP
```

---

