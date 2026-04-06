OSI Model & Networking Notes
OSI Model Overview

The OSI model provides a framework dictating how all networked devices send, receive, and interpret data.

OSI Layers
Layer	Name	Description
1	Physical	hardware components (e.g., Ethernet cable)
2	Data Link	physical addressing using MAC
3	Network	routing using IP
4	Transport	data transfer (TCP/UDP)
5	Session	session management
6	Presentation	encryption and formatting
7	Application	user interaction
Layer Details
Physical
physical components of networking
example: Ethernet cable
Data Link
physical addressing of transmission
packet contains IP info and is mapped to MAC address
NIC provides a unique MAC address
Network
determines optimal routing path
protocols:
OSPF (Open Shortest Path First)
RIP (Routing Information Protocol)
routers are Layer 3 devices
Transport
Protocol	Behavior
TCP	reliable, ordered
UDP	fast, no guarantee
Example: Cat Image (4 chunks)
Protocol	Result
TCP	image only if all chunks received
UDP	displays whatever is received
Session
connection creates a session
Presentation
handles encryption (e.g., HTTPS)
Application
user interacts with data via GUI
defines rules for communication
Packets vs Frames
Term	Meaning
Packet	contains IP address
Frame	encapsulated structure

Analogy:

Frame = envelope
Packet = letter
TCP
ensures correct and ordered delivery
slower but reliable
TCP/IP Model
Layer	Function
Application	HTTP, FTP
Transport	TCP, ports
Internet	IP addressing
Network Interface	physical transfer
Encapsulation
sender adds headers
receiver removes headers
TCP Reliability
sequence numbers
acknowledgements (ACK)
checksum
retransmission
TCP Headers
Field	Purpose
Source Port	sender
Destination Port	receiver
Source IP	sender address
Destination IP	receiver address
Sequence Number	order
Acknowledgement Number	confirmation
Checksum	integrity
Flags	SYN, ACK, FIN, RST
Data	payload
Three-Way Handshake
Step	Action
1	SYN
2	SYN-ACK
3	ACK

Connection established.

Data Transfer
data sent with sequence numbers
ACK confirms receipt
missing data is resent
Connection Closing
Step	Action
1	FIN
2	ACK
3	FIN
4	ACK

Flow:
SYN → SYN-ACK → ACK → DATA → FIN → ACK

UDP
Overview
Feature	Description
Type	connectionless
Reliability	none
Speed	very fast
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
no guarantee of delivery
no order
no recovery
UDP Headers
Field	Purpose
Source IP	sender
Destination IP	receiver
Source Port	random
Destination Port	fixed
TTL	lifetime
Data	payload
UDP Flow
sender sends data
receiver may or may not receive
no acknowledgement
TCP vs UDP
TCP: Connect → Check → Deliver → Confirm
UDP: Send → Hope → Done
Ports
Range	Description
0–1024	common ports
0–65535	total ports

Reference: https://www.vmaxx.net/techinfo/ports.htm

Port Forwarding
connects internal services to the internet
required for web servers
configured on a router
Firewall

A firewall controls network traffic using packet inspection.

Type	Behavior
Stateful	analyzes full connection
Stateless	analyzes individual packets
VPN (Virtual Private Network)
creates a secure tunnel over the internet
connects remote networks
provides privacy
VPN Technologies
Technology	Function
PPP	authentication and encryption
PPTP	allows PPP to leave network
IPSec	encrypts using IP framework
