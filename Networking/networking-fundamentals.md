OSI Model & Networking Notes
OSI Model

The OSI model provides a framework dictating how networked devices send, receive, and interpret data.

OSI Layers (7 Layers)
1. Physical
physical components of networking
example: Ethernet cable
2. Data Link
handles physical addressing
packet contains IP info → mapped to MAC address
NIC provides a unique MAC address
3. Network
determines optimal routing path
uses protocols:
OSPF (Open Shortest Path First)
RIP (Routing Information Protocol)
routers operate at Layer 3
4. Transport
TCP (Transmission Control Protocol)
data split into small chunks
requires all chunks to be received
ensures order and accuracy
used in:
file sharing
web browsing
email
UDP (User Datagram Protocol)
data split into chunks
sends without checking
no guarantee of delivery or order
Example (Cat Image)
split into 4 chunks

TCP:

checks all chunks and order
missing chunk → no image

UDP:

displays whatever is received
ignores missing or unordered chunks
5. Session
session is created when connection is established
6. Presentation
handles encryption (e.g., HTTPS)
7. Application
user interacts with data
provides GUI and communication rules
Packets vs Frames

Think of sending a letter:

Frame → envelope
Packet → actual message

Rule:

data with IP address → Packet
without IP address → Frame
TCP
reliable and ordered delivery
slower than UDP
Why TCP is Reliable
sequence numbers
acknowledgements (ACK)
checksum
retransmission
TCP Headers
Source Port
Destination Port
Source IP
Destination IP
Sequence Number
Acknowledgement Number
Checksum
Flags (SYN, ACK, FIN, RST)
Data
Three-Way Handshake
SYN → SYN-ACK → ACK

Connection established.

Data Transfer
data sent with sequence numbers
receiver sends ACK
missing data is resent
Connection Closing
FIN → ACK → FIN → ACK
TCP/IP Model (4 Layers)
Application → HTTP, FTP
Transport → TCP
Internet → IP
Network Interface → physical transfer
Encapsulation
sender adds headers while moving down layers
receiver removes headers
UDP
Key Characteristics
connectionless
no handshake
no guarantees
very fast
Behavior
stateless
no ACK
no retransmission
Use Cases
video streaming
voice calls
online gaming
live broadcast
Advantages
fast
low overhead
works on unstable networks
Disadvantages
no delivery guarantee
no order
no error recovery
UDP Headers
Source IP
Destination IP
Source Port
Destination Port
TTL
Data
UDP Flow
Send → Maybe Received → Done
TCP vs UDP
TCP: Connect → Check → Deliver → Confirm
UDP: Send → Hope → Done
Ports
range: 0 – 65535
common ports: 0 – 1024

Reference:
https://www.vmaxx.net/techinfo/ports.htm

Port Forwarding
connects internal services to the internet
required for web servers
configured on router
Firewall

Controls incoming and outgoing traffic.

Types
Stateful → analyzes full connection
Stateless → analyzes individual packets
VPN (Virtual Private Network)
creates a secure tunnel over the internet
connects different networks
provides privacy
VPN Technologies
PPP → authentication + encryption (cannot leave network alone)
PPTP → allows PPP to travel outside network
IPSec → encrypts using IP framework
