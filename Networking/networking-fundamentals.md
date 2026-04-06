The OSI model (or Open Systems Interconnection Model)
provides a framework dictating how all networked devices will send, receive and interpret data.
The OSI model consists of seven layers.

1.physical
the physical components of the hardware used in networking
ex: Ethernet cable

2.data link
the physical addressing of the transmission
-it sends packet containing info of host computer(ip address) and add that in mac address of receiving computer.
-Inside every network-enabled computer is a Network Interface Card (NIC) which comes with a unique MAC address to identify it.

3.network
-routing simply determines the most optimal path in which these chunks of data should be sent.
-it use protocols, OSPF (Open Shortest Path First) and RIP (Routing Information Protocol).
-Devices such as routers capable of delivering packets using IP addresses are known as Layer 3 devices — because they are capable of        	working at the third layer of the OSI model.

4.transport
When data is sent between devices uses two different protocol
 	1.Transmission Control Protocol (TCP)
      		in this, if there is a file ,it will be shared in small chunks.
       		-If one small chunk of data is not received, then the entire chunk of data cannot be used.
       		-TCP is used for situations such as file sharing, internet browsing or sending an email. This usage is because these 			services
 		require the data to be accurate and complete (no good having half a file!

 	2.User Datagram Protocol (udp)
        in this, if there is a file ,it will be shared in small chunks.
 	-it send all the chunks, does not care do the computer is receiving it.
 	-if computer receives half a chunks, it will show them.

ex: if we are sharing cat image:
 	-it will be shared in 4 chunks
 
 	1.TCP: this protocol will check
 		-do all the chunk are received and there order. If yes: it will show image.
 		-if even single chunk is not present: it will not generate image.

        2.UDP: it will not care do all chunks are received or not.
 		it will just generate ,which is received.
 		-will not ensure, presence of all the chunks or there order.


5.session
 	-When a connection is established, a session is created
6.presentation
 	-Security features such as data encryption (like HTTPS when visiting a secure site) occur at this layer.
7.application
 	-the layer in which protocols and rules are in place to determine how the user should interact with data sent or received.
 	-provide a friendly, Graphical User Interface (GUI) for users to interact with data sent or received.




Packets and Frames

You can think of this process as similar to mailing a letter through the post. The envelope is a frame, which, is used to move the contents (in this analogy, the packet) of the envelope to another place. Once the recepient opens the envelop (frame), they will know how to forward the letter (packet) itself.
assume that when we are talking about anything IP addresses, we are talking about packets. When the encapsulating information is stripped away, we're talking about the frame itself.


in short
if the peace of data have iP address - Packet
                 not have iP address - Frame



TCP    



-Ensures data is delivered correctly and in order.

-Slower than UDP, but reliable.



TCP/IP Model (4 Layers)

Application – User-facing services (HTTP, FTP, etc.)

Transport – Handles ports, sequencing, reliability (TCP lives here)

Internet – Logical addressing (IP)

Network Interface – Physical data transfer




Key Idea: Encapsulation

Data moves down the layers → headers added.

Receiver removes headers → decapsulation.



Why TCP is Reliable

Uses sequence numbers to order data.

Uses ACKs to confirm delivery.

Uses checksum to detect corruption.

Resends lost data automatically.



Important TCP Headers (Remember the Core)

Source Port – Sender’s port

Destination Port – Service port (e.g., 80)

Source IP / Destination IP – Sender & receiver addresses

Sequence Number – Order of data

Acknowledgement Number – Confirms received data

Checksum – Data integrity

Flags – Control connection (SYN, ACK, FIN, RST)

Data – Actual payload



Three-Way Handshake (Connection Setup)

SYN – Client: “Can we talk?”

SYN-ACK – Server: “Yes, and I hear you.”

ACK – Client: “Confirmed. Start sending data.”

➡ Connection established.

Data Transfer

-Data sent with sequence numbers.

-Receiver sends ACK for each part.

-Missing data → re-sent.

-Closing the Connection

FIN – Device requests to close.

ACK – Other device confirms.

FIN – Other side also closes.

ACK – Final confirmation.

➡ Connection closed cleanly.
SYN → SYN-ACK → ACK → DATA → FIN → ACK


UDP
UDP — Process Summary (Short & Simple)

What UDP is

Connectionless protocol.
No handshake. No guarantees.
Speed over reliability.



Core Behavior
   Stateless – no session, no tracking.
   Data is sent and forgotten.
   Receiver does not acknowledge delivery.


When UDP Is Used
   Video streaming
   Voice calls
   Online gaming
   Live broadcasts
   (Where speed matters more than perfection.)


Why UDP Is Fast
    No connection setup.
    No error checking.
    No re-transmission.
    Minimal processing.
    Advantages (Think: Speed)
    Very fast.
    Low overhead.
    Works even on unstable networks.
    No resource reservation on devices.



Disadvantages (Think: Risk)
    No guarantee data is received.
    No order checking.
    No error recovery.
    Packet loss = data loss.



UDP Packet Headers (Only the Essentials)
      Source IP – Sender’s address
      Destination IP – Receiver’s address
      Source Port – Sender’s port (random)
      Destination Port – Service port (fixed)
      TTL – Packet lifetime limit
      Data – Actual payload



UDP Communication Flow
      Sender sends data.
      Receiver may get it—or may not.
      No ACK.
      No retry.
      Sender moves on.




TCP vs UDP — Memory Hook

TCP: Connect → Check → Deliver → Confirm
UDP: Send → Hope → Done



PORT 101

 ports are a numerical value between 0 and 65535 (65,535).
 . Any port that is within 0 and 1024 (1,024) is known as a common port.
https://www.vmaxx.net/techinfo/ports.htm(LIST OF PORTS)



Port forwarding is an essential component in connecting applications and services to the Internet. Without port forwarding, applications and services such as web servers are only available to devices within the same direct network.
the name of the device that is used to configure port forwarding is router.


A firewall is a device within a network responsible for determining what traffic is allowed to enter and exit.
Firewalls perform packet inspection 


1.Stateful:firewall uses the entire information from a connection; rather than inspecting an individual packet, this firewall determines       		the behaviour of a device based upon the entire connection.

2.stateless:firewall inspects individual packets



A Virtual Private Network (or VPN for short) is a technology that allows devices on separate networks to communicate securely by creating a dedicated path between each other over the Internet (known as a tunnel). Devices connected within this tunnel form their own private network.
Allows networks in different geographical locations to be connected.
Offers privacy.

VPN TECHNOLOGY:

1.PPP: allow for authentication and provide encryption of data.(CAN NOT leave network on its own.)
2.PPTP: the technology that allows the data from PPP to travel and leave a network. 
3.IPSec: Internet Protocol Security (IPsec) encrypts data using the existing Internet Protocol (IP) framework.
