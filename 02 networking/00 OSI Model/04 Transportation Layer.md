## Overview
The Transport Layer (Layer 4 in the OSI model) is responsible for end-to-end communication. 
It ensures that data is reliably transferred between devices. 
This layer handles error checking, flow control, and retransmission of lost packets.

The main protocols in this layer are:
- [[#1. TCP (Transmission Control Protocol)|TCP]]
- [[#2. UDP (User Datagram Protocol)|UDP]]
- [[#3. IP (Internet Protocol)|IP]] (used with TCP and UDP at this layer for routing).

### Functions of the Transport Layer:
- **Reliable Data Transfer**: Ensures data is received correctly and completely.
- **Segmentation**: Breaks large messages into smaller segments for easier transmission. These are then reassembled at the destination.
- **Flow Control**: Manages the rate of data transmission to prevent the receiver from being overwhelmed.
- **Error Detection and Correction**: Verifies data integrity and corrects errors if necessary.
- **Multiplexing and Demultiplexing**: Uses port numbers to differentiate between multiple applications on the same device, allowing simultaneous connections.

---

## Key Protocols

### **1. TCP (Transmission Control Protocol)**
- **Overview**: 
  - [[#1. TCP (Transmission Control Protocol)|TCP]] is a connection-oriented protocol. 
  - It establishes a reliable connection between sender and receiver before data transmission begins.
  - TCP ensures data is delivered accurately and in the correct order. 
  - This makes it suitable for applications where reliability is critical.
- **Features**:
	- **Connection-Oriented**: Requires a handshake (SYN, SYN-ACK, ACK) to establish a connection before data transfer begins.
	- **Reliable Transmission**: Guarantees data delivery by retransmitting lost packets and verifying data integrity with checksums.
	- **Ordered Delivery**: Ensures that data arrives in the correct order by reassembling packets at the receiver.
	- **Flow Control**: Uses a sliding window mechanism to control data flow and prevent buffer overflow at the receiver.
- **TCP Handshake**:
    1. **SYN**: Client sends a SYN (synchronize) message to initiate a connection.
    2. **SYN-ACK**: Server responds with a SYN-ACK to acknowledge the connection.
    3. **ACK**: Client sends an ACK to complete the connection setup.
- **TCP Connection Termination**:
    - A four-step process where both client and server exchange **FIN** and **ACK** messages to terminate the connection.
- **Use Cases**: TCP is used in applications that prioritize data accuracy and reliability:
    - **HTTP/HTTPS**: Web browsing
    - **FTP**: File transfers
    - **SMTP**: Email

---

### **2. UDP (User Datagram Protocol)**
- **Overview**: 
  - [[#2. UDP (User Datagram Protocol)|UDP]] is a connectionless protocol.
  - It prioritizes speed over reliability.
  - Unlike TCP, it does not establish a connection before sending data.
  - Suitable for applications where low latency is critical and occasional data loss is acceptable.
- **Features**:
	- **Connectionless**: No handshake is required; data is sent without establishing a connection, making it faster.
	- **Unreliable Transmission**: Does not guarantee delivery, order, or error correction, trading reliability for speed.
	- **Low Latency**: Ideal for applications where data must be transmitted quickly.
- **UDP Packet Structure**:
	- **Source Port**: Identifies the sending port.
	- **Destination Port**: Identifies the receiving port.
	- **Length**: Specifies the length of the UDP header and data.
	- **Checksum**: Provides basic error-checking (optional).
- **Use Cases**: UDP is used in applications where speed is more important than reliability:
	- **Video Streaming**: Live broadcasts, video calls
	- **Online Gaming**: Fast-paced games requiring minimal delay
	- **DNS Queries**: Quickly resolving domain names

---

## **3. IP (Internet Protocol)**
- **Overview**: 
  - [[#3. IP (Internet Protocol)|IP]] is responsible for addressing and routing data across networks.
  - It works in conjunction with TCP and UDP to send data packets to the correct destination.
  - IP operates at both the Network and Transport layers. 
  - It assigns unique addresses and determines the best path for packets to reach their destination.
- **Functions**:
	- **Addressing**: Assigns unique IP addresses to devices, allowing data to reach the correct destination.
	- **Packetization**: Breaks down data into smaller packets for efficient transmission over the network.
	- **Routing**: Determines the best path for packets to travel through various networks, using routers to direct packets based on IP addresses.
- **Versions**:
	- **IPv4**: Uses 32-bit addresses (e.g., 192.168.1.1) with around 4.3 billion unique addresses.
	- **IPv6**: Uses 128-bit addresses (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334), designed to accommodate the expanding number of internet-connected devices.
- **Key Concepts**:
	- **Subnetting**: Divides an IP address space into smaller, manageable networks for efficient routing and security.
	- **NAT (Network Address Translation)**: Allows private IP addresses within a local network to communicate with the internet using a single public IP.

