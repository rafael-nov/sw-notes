
### Summary

- **Layers 1-4** focus on data transport.
- **Layers 5-7** focus on application support and user interactions.
- **Mnemonic to Remember**: *"Please Do Not Throw Sausage Pizza Away"* 
	- (Physical, Data Link, Network, Transport, Session, Presentation, Application).
---

### Overview
The OSI (Open Systems Interconnection) model is a conceptual framework used to understand and implement network interactions. 
It divides network communication into **7 layers**, each with specific functions. 
Understanding the OSI model helps in troubleshooting network issues, as each layer can be isolated.

| Layer | Name                   | Description                                                                                  |
| ----- | ---------------------- | -------------------------------------------------------------------------------------------- |
| 1     | **Physical Layer**     | Deals with raw bit transmission over the physical medium.                                    |
| 2     | **Data Link Layer**    | Handles physical addressing and error detection. Protocols: Ethernet, PPP.                   |
| 3     | **Network Layer**      | Routes packets across networks. Protocols: IP, ICMP.                                         |
| 4     | **Transport Layer**    | Ensures data transfer reliability with error-checking and flow control. Protocols: TCP, UDP. |
| 5     | **Session Layer**      | Manages sessions/connections between applications. Protocols: RPC, PPTP.                     |
| 6     | **Presentation Layer** | Translates, encrypts, and compresses data. Formats data for the app layer.                   |
| 7     | **Application Layer**  | Interfaces with end-user applications. Protocols: HTTP, FTP, SMTP, etc.                      |

---

### Layer Descriptions

# OSI Model: Lower Layers Protocols and Functions

 1. [[01 Physical Layer]]
	- **Function**: 
		- Transmits raw binary data (0s and 1s) over the physical medium. 
		- It defines the hardware elements involved in data transmission, such as electrical signals, light pulses, or radio waves. 
		- The Physical Layer specifies the characteristics of cables, connectors, voltage levels, and data transmission rates.
	- **Devices**:
		  - **Hubs**: Basic networking devices that connect multiple devices in a network segment, broadcasting data to all connected devices.
		  - **Cables**: Mediums for physical data transfer, such as twisted pair, coaxial, and fiber optic cables.
		  - **Repeaters**: Amplify signals to extend the distance data can travel over a network by compensating for signal degradation.
	- **Characteristics**:
		  - **Data Rate (Bandwidth)**: Determines the speed at which data is transmitted.
		  - **Signal Type**: Electrical (copper cables), optical (fiber optic), or electromagnetic (wireless).
		  - **Topology**: Physical layout of devices in the network (e.g., star, bus, ring).

---
2. [[02 Data Link Layer]]
	- **Function**: 
		- Manages node-to-node data transfer, providing error detection and flow control. 
		- The Data Link Layer ensures reliable communication between devices on the same local network by packaging data into frames.
	- **Sub-layers**:
		  - **LLC (Logical Link Control)**: Manages frame synchronization, flow control, and error checking.
		  - **MAC (Media Access Control)**: Controls how devices on the network gain access to the physical medium and permission to transmit data.
	- **Devices**:
		  - **Switches**: Operate at the Data Link Layer, forwarding data based on MAC addresses to ensure it reaches the correct destination within a local network.
		  - **Bridges**: Connect multiple network segments within the same network, filtering traffic to reduce congestion and extend the network's range.
	- **Protocols**:
		  - **Ethernet**: A widely used protocol that defines standards for wiring and signaling at the Data Link Layer.
		  - **PPP (Point-to-Point Protocol)**: Used for direct communication between two nodes, often in dial-up and DSL connections.
	- **Functions**:
		  - **Error Detection**: Detects errors in frames (e.g., using cyclic redundancy check - CRC).
		  - **Flow Control**: Manages the pace of data transmission between devices to prevent overload.

---
3. [[03 Network Layer]]
	- **Function**: 
		- Determines the best path for data to travel across networks. 
		- It’s responsible for logical addressing, routing, and packet forwarding between devices on different networks.
	- **Protocols**:
		  - **IP (Internet Protocol)**: Defines the addressing scheme and is responsible for routing packets from source to destination across multiple networks.
		  - **ICMP (Internet Control Message Protocol)**: Used for sending error messages and operational information, such as when a service is unavailable or a router cannot be reached (e.g., `ping` command).
		  - **IGMP (Internet Group Management Protocol)**: Manages multi-casting, allowing a device to send a single packet to multiple destinations.
	- **Devices**:
		  - **Routers**: Forward packets between networks by using IP addresses to determine the best path to the destination.
	- **Functions**:
		  - **Routing**: Determines the optimal path to forward packets based on routing algorithms (e.g., Dijkstra’s algorithm).
		  - **Logical Addressing**: Provides unique IP addresses for each device on a network to enable proper packet forwarding.

---
 4. [[04 Transportation Layer]]
	- **Function**: 
		- Ensures reliable data transfer between devices by providing error-checking, flow control, and re-transmission of lost data packets when necessary. 
		- It segments data into smaller units for easier handling and reassembles it at the destination.
	- **Protocols**:
		  - **TCP (Transmission Control Protocol)**: 
			  - A connection-oriented protocol that establishes a reliable connection before data is sent. 
			  - TCP ensures that data arrives in order and retransmits any lost packets.
		  - **UDP (User Datagram Protocol)**: 
			  - A connectionless protocol that prioritizes speed over reliability. 
			  - UDP is commonly used for time-sensitive applications where minor data loss is acceptable, such as video streaming or online gaming.
	- **Devices**:
		  - **Firewalls** (at transport level): 
			  - Control and filter network traffic based on transport layer protocols and port numbers. 
			  - They can block or allow packets depending on security policies.
	- **Functions**:
		  - **Segmentation**: Breaks large data units into smaller segments, making it easier to manage and reassemble.
		  - **Flow Control**: Ensures that the sender does not overwhelm the receiver by adjusting the rate of data transmission.
		  - **Error Checking**: Uses checksums to verify data integrity.
		  - **Retransmission**: Retransmits lost or corrupted packets (mainly in TCP) to ensure reliable data delivery.

---
5. [[05 Session Layer]]
	- **Function**: 
		- Manages and controls connections between applications, responsible for setting up, managing, and terminating sessions. 
	- **Common Protocols**: 
		- **PPTP** (Point-to-Point Tunneling Protocol) - Tunneling protocol for creating virtual private networks. 
		- **RPC** (Remote Procedure Call) - Allows a program to execute code on another computer. 
		- **NetBIOS** (Network Basic Input/Output System) - Enables applications on different computers to communicate within a local network. 
		- **SOCKS** - Proxy protocol used to route network packets between client and server through a proxy server.

---
6. [[06 Presentation Layer]]
	- **Function**: 
		- Translates, encrypts, and compresses data, making it readable by the Application Layer. 
	- **Common Formats and Protocols**: 
		- **SSL/TLS** (Secure Sockets Layer / Transport Layer Security) - Encrypts data for secure communication. 
		- **MIME** (Multipurpose Internet Mail Extensions) - Specifies types of content in emails, like text, images, and video. 
		- **JPEG, PNG, GIF** - Image compression formats. 
		- **MP3, AAC** - Audio compression formats. 
		- **ASCII, EBCDIC** - Character encoding standards. 
		- **XML, JSON** - Data formats for structured information exchange.

---
7. [[07 Application Layer]]
   - **Function**: 
	   - Provides network services directly to end-user applications.
   - **Protocols**: 
		- **HTTP** (Hypertext Transfer Protocol) - Used for web communication between clients and servers. 
		- **HTTPS** (HTTP Secure) - Secure version of HTTP using SSL/TLS. 
		- **FTP** (File Transfer Protocol) - Used for transferring files between computers. 
		- **SMTP** (Simple Mail Transfer Protocol) - Used for sending emails. 
		- **IMAP** (Internet Message Access Protocol) - Protocol for accessing and managing email on a server. 
		- **POP3** (Post Office Protocol 3) - Retrieves emails from a server to a client. 
		- **DNS** (Domain Name System) - Translates domain names to IP addresses. 
		- **Telnet** - Provides bidirectional interactive communication over a network. 
		- **SSH** (Secure Shell) - Encrypts network services for secure remote login and command execution. 
		- **LDAP** (Lightweight Directory Access Protocol) - Accesses and maintains distributed directory information services. 
		- **NTP** (Network Time Protocol) - Synchronizes clocks over a network. 
		- **DHCP** (Dynamic Host Configuration Protocol) - Assigns IP addresses dynamically to devices on a network. 
		- **SNMP** (Simple Network Management Protocol) - Manages and monitors network devices. 
		- **SIP** (Session Initiation Protocol) - Used to initiate, maintain, and terminate real-time sessions (e.g., VoIP calls). 
		- **IRC** (Internet Relay Chat) - Used for real-time messaging between users. 
		- **RTP** (Real-time Transport Protocol) - Used for delivering audio and video over IP networks.

---
### Why the OSI Model is Important

- **Troubleshooting**: Helps isolate issues to specific layers (e.g., if ping works but HTTP doesn’t, it’s likely an application or transport layer issue).
- **Standardization**: Provides a universal reference for networking protocols, making it easier to understand and develop compatible technologies.

---


