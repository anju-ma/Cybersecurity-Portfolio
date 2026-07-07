# TCP/IP (Transmission Control Protocol/Internet Protocol) Model

## 1. What is the TCP/IP Model?

The **TCP/IP (Transmission Control Protocol/Internet Protocol) Model** is a network communication model that defines how devices communicate over a network and the Internet.

It divides network communication into **four layers**, with each layer performing a specific function.

> **Note:** Unlike the OSI model, the TCP/IP model is based on the actual protocols used in modern computer networks and forms the foundation of the Internet.

---

## 2. Why Do We Need the TCP/IP Model?

The TCP/IP model helps to:

- Standardize network communication.
- Enable communication between different devices and operating systems.
- Form the foundation of the Internet.
- Simplify network design and troubleshooting.

---

## 3. The Four Layers of the TCP/IP Model

### Layer 4 – Application Layer

**Purpose**

Provides network services directly to user applications.

This layer combines the functions of the **Application, Presentation, and Session** layers of the OSI model.

**Common Protocols**

- HTTP
- HTTPS
- FTP
- SMTP
- POP3
- IMAP
- DNS
- DHCP
- SSH

**Data Unit**

- Data

**Example**

Opening a website or sending an email.

---

### Layer 3 – Transport Layer

**Purpose**

Provides end-to-end communication between applications.

**Common Protocols**

- TCP
- UDP

**Data Unit**

- Segment (TCP)
- Datagram (UDP)

**Example**

Reliable file transfer using TCP or live video streaming using UDP.

---

### Layer 2 – Internet Layer

**Purpose**

Provides logical addressing and routes packets between different networks.

**Common Protocols**

- IPv4
- IPv6
- ICMP
- IGMP

**Devices**

- Router
- Layer 3 Switch

**Address**

- IP Address

**Data Unit**

- Packet

**Example**

Routing packets across the Internet.

---

### Layer 1 – Network Access Layer (Link Layer)

**Purpose**

Handles communication over the local network and transmits data through the physical network medium.

**Common Protocols**

- Ethernet
- Wi-Fi (IEEE 802.11)
- ARP

**Devices**

- NIC
- Switch
- Hub
- Access Point

**Address**

- MAC Address

**Data Unit**

- Frame

**Example**

Sending data between devices on the same local network.

---

## 4. TCP/IP Model Summary

| Layer | Main Function | Examples | Data Unit |
|--------|---------------|----------|-----------|
| Application | Network services for applications | HTTP, HTTPS, DNS | Data |
| Transport | End-to-end communication | TCP, UDP | Segment / Datagram |
| Internet | Logical addressing and routing | IPv4, IPv6, ICMP | Packet |
| Network Access | Local network communication | Ethernet, Wi-Fi, ARP | Frame |

---

## 5. Data Encapsulation

When data is transmitted, each layer adds its own header before passing the data to the next layer.

```text
Application → Data
        ↓
Transport → Segment
        ↓
Internet → Packet
        ↓
Network Access → Frame
        ↓
Physical Medium
```

At the receiving device, the reverse process (**decapsulation**) removes the headers layer by layer until the original data reaches the application.

---

## 6. Example: Opening a Website

When you visit **https://www.example.com**:

1. The **Application Layer** creates an HTTPS request.
2. The **Transport Layer** uses TCP to establish a connection and divide the data into segments.
3. The **Internet Layer** adds the source and destination IP addresses.
4. The **Network Access Layer** adds the source and destination MAC addresses and transmits the data over the network.

---

## 7. TCP/IP vs OSI Model

| OSI Model | TCP/IP Model |
|------------|--------------|
| Application | Application |
| Presentation | Application |
| Session | Application |
| Transport | Transport |
| Network | Internet |
| Data Link | Network Access |
| Physical | Network Access |

---

## 8. Advantages

- Foundation of the Internet.
- Widely used in modern networks.
- Simple and practical design.
- Supports communication between different devices and operating systems.

---

## 9. Limitations

- Less detailed than the OSI model.
- Does not separate the Presentation and Session functions into individual layers.

---

## 10. Cybersecurity Relevance

Understanding the TCP/IP model helps cybersecurity professionals identify attacks at different layers.

| Layer | Example Threat |
|--------|----------------|
| Application | HTTP attacks, DNS attacks, Phishing |
| Transport | TCP SYN Flood, UDP Flood, Port Scanning |
| Internet | IP Spoofing, ICMP Attacks |
| Network Access | ARP Spoofing, MAC Flooding |

SOC analysts use the TCP/IP model to analyze network traffic, investigate incidents, and understand how attacks move through a network.

---

## 11. Key Takeaways

- The TCP/IP model divides network communication into four layers.
- It is the practical networking model used on modern networks and the Internet.
- Each layer has a specific responsibility and uses different protocols.
- Data is encapsulated before transmission and decapsulated at the destination.
- Understanding the TCP/IP model is essential for networking and cybersecurity.
