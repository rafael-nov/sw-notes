- [[#HTTP (Hypertext Transfer Protocol)]]
- [[#HTTPS (HTTP Secure)]]
- [[#FTP (File Transfer Protocol)]]
- [[#SMTP (Simple Mail Transfer Protocol)]]
- [[#IMAP (Internet Message Access Protocol)]]
- [[#POP3 (Post Office Protocol 3)]]
- [[#DNS (Domain Name System)]]
- [[#Telnet]]
- [[#SSH (Secure Shell)]]
- [[#LDAP (Lightweight Directory Access Protocol)]]
- [[#NTP (Network Time Protocol)]]
- [[#DHCP (Dynamic Host Configuration Protocol)]]
- [[#SNMP (Simple Network Management Protocol)]]
- [[#SIP (Session Initiation Protocol)]]
- [[#IRC (Internet Relay Chat)]]
- [[#RTP (Real-time Transport Protocol)]]

---
## Protocol Descriptions

### HTTP (Hypertext Transfer Protocol)
- **Function**: Used for web communication between clients (browsers) and servers.
- **Key Points**:
    - Operates on port 80.
    - Transmits web content (HTML, images, etc.) without encryption.
    - Foundation of data exchange on the World Wide Web.

### HTTPS (HTTP Secure)
- **Function**: Secure version of HTTP using SSL/TLS encryption.
- **Key Points**:
    - Operates on port 443.
    - Encrypts web traffic to protect sensitive information.
    - Widely used for secure web browsing (e.g., online banking, e-commerce).

### FTP (File Transfer Protocol)
- **Function**: Transfers files between computers over a network.
- **Key Points**:
    - Operates on ports 20 and 21.
    - Supports file upload and download but lacks encryption.
    - Commonly used for managing website files.

### SMTP (Simple Mail Transfer Protocol)
- **Function**: Sends emails between mail servers.
- **Key Points**:
    - Operates on port 25.
    - Transports outgoing mail from clients to servers and between mail servers.
    - Often works with protocols like IMAP or POP3 for retrieving emails.

### IMAP (Internet Message Access Protocol)
- **Function**: Accesses and manages email on a server.
- **Key Points**:
    - Operates on port 143 (unencrypted) or 993 (encrypted).
    - Allows multiple devices to access the same email account.
    - Enables synchronization of email folders across devices.

### POP3 (Post Office Protocol 3)
- **Function**: Retrieves emails from a server to a client.
- **Key Points**:
    - Operates on port 110 (unencrypted) or 995 (encrypted).
    - Downloads emails to the local device, usually deleting them from the server.
    - Often used for accessing email offline.

### DNS (Domain Name System)
- **Function**: Translates domain names to IP addresses.
- **Key Points**:
    - Operates on port 53.
    - Converts user-friendly URLs into IP addresses for networking.
    - Essential for navigating the internet by name rather than IP.

### Telnet
- **Function**: Provides bidirectional interactive communication over a network.
- **Key Points**:
    - Operates on port 23.
    - Used for remote access to devices, but lacks encryption.
    - Mostly replaced by SSH for secure connections.

### SSH (Secure Shell)
- **Function**: Encrypts network services for secure remote login and command execution.
- **Key Points**:
    - Operates on port 22.
    - Provides secure access to servers and network devices.
    - Widely used for secure administration and remote control.

### LDAP (Lightweight Directory Access Protocol)
- **Function**: Accesses and maintains distributed directory information services.
- **Key Points**:
    - Operates on port 389 (unencrypted) or 636 (encrypted).
    - Manages user and resource information, such as login credentials and permissions.
    - Often used in corporate networks for user authentication.

### NTP (Network Time Protocol)
- **Function**: Synchronizes clocks over a network.
- **Key Points**:
    - Operates on port 123.
    - Ensures accurate timekeeping across devices.
    - Vital for time-sensitive applications and log consistency.

### DHCP (Dynamic Host Configuration Protocol)
- **Function**: Assigns IP addresses dynamically to devices on a network.
- **Key Points**:
    - Operates on ports 67 and 68.
    - Automates IP address assignment and management.
    - Commonly used in home and enterprise networks.

### SNMP (Simple Network Management Protocol)
- **Function**: Manages and monitors network devices.
- **Key Points**:
    - Operates on ports 161 and 162.
    - Collects information about network performance and health.
    - Used for centralized network management.

### SIP (Session Initiation Protocol)
- **Function**: Initiates, maintains, and terminates real-time sessions (e.g., VoIP calls).
- **Key Points**:
    - Operates on ports 5060 (unencrypted) and 5061 (encrypted).
    - Commonly used in voice and video communications.
    - Manages the setup and teardown of calls.

### IRC (Internet Relay Chat)
- **Function**: Used for real-time messaging between users.
- **Key Points**:
    - Operates on port 6667 or custom ports.
    - Supports chat rooms and private messaging.
    - Used in various online communities and for quick communication.

### RTP (Real-time Transport Protocol)
- **Function**: Delivers audio and video over IP networks.
- **Key Points**:
    - Often used alongside SIP for streaming media in real-time.
    - Provides end-to-end network transport for real-time applications.
    - Supports applications like video conferencing and live broadcasts.
