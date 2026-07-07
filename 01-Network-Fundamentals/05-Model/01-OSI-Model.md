# OSI (Open Systems Interconnection) Model

## 1. What is the OSI Model?

The **OSI (Open Systems Interconnection) Model** is a **conceptual framework** developed by the **International Organization for Standardization (ISO)** to standardize network communication.

It divides network communication into **seven layers**, where each layer performs a specific function and communicates with the layers directly above and below it.

> **Note:** The OSI model is mainly used for learning, designing, and troubleshooting networks. Modern networks primarily use the **TCP/IP model**, but the OSI model remains essential for understanding networking concepts.

---

## 2. Why Do We Need the OSI Model?

The OSI model simplifies network communication by dividing it into separate layers.

It helps to:

- Break networking into smaller, manageable parts.
- Simplify troubleshooting.
- Standardize communication between different vendors.
- Improve network design and development.
- Help engineers identify where network problems occur.

---

## 3. The Seven Layers of the OSI Model

### Layer 7 – Application

**Purpose**

Provides network services directly to end-user applications.

**Common Protocols**

- HTTP
- HTTPS
- FTP
- SMTP
- DNS
- DHCP
- SSH

**Data Unit**

- Data

**Example**

Opening a website or sending an email.

---

### Layer 6 – Presentation

**Purpose**

Prepares data for the Application Layer by performing:

- Data translation
- Encryption and decryption
- Compression and decompression

**Data Unit**

- Data

**Example**

Encrypting data for an HTTPS connection.

---

### Layer 5 – Session

**Purpose**

Establishes, manages, and terminates communication sessions between applications.

**Data Unit**

- Data

**Example**

Maintaining a video conference session.

---

### Layer 4 – Transport

**Purpose**

Provides end-to-end communication between applications.

**Common Protocols**

- TCP
- UDP

**Data Unit**

- Segment (TCP)
- Datagram (UDP)

**Example**

Reliable file transfer using TCP or live streaming using UDP.

---

### Layer 3 – Network

**Purpose**

Routes packets between different networks using IP addresses.

**Devices**

- Router
- Layer 3 Switch

**Address**

- IP Address

**Data Unit**

- Packet

**Example**

Routing traffic across the Internet.

---

### Layer 2 – Data Link

**Purpose**

Provides node-to-node communication within the same Local Area Network (LAN) using MAC addresses.

**Devices**

- Switch
- Bridge
- NIC

**Address**

- MAC Address

**Data Unit**

- Frame

**Example**

Sending data between devices on the same LAN.

---

### Layer 1 – Physical

**Purpose**

Transmits raw bits over the physical communication medium such as cables, fiber optics, or wireless signals.

**Devices**

- Hub
- Repeater
- Cables
- Connectors

**Data Unit**

- Bits

**Example**

Transmitting electrical, optical, or radio signals.

---

## 4. OSI Layers Summary

| Layer | Name | Data Unit | Address | Examples |
|------:|----------------|-----------|----------------|----------------|
| 7 | Application | Data | — | HTTP, HTTPS |
| 6 | Presentation | Data | — | Encryption, Compression |
| 5 | Session | Data | — | Session Management |
| 4 | Transport | Segment / Datagram | Port Number | TCP, UDP |
| 3 | Network | Packet | IP Address | IP, ICMP |
| 2 | Data Link | Frame | MAC Address | Ethernet |
| 1 | Physical | Bits | — | Cables, Fiber Optic, Wi-Fi |

---

## 5. Data Encapsulation

When data is transmitted, each layer adds its own header before passing the data to the next layer.

```text
Application → Data
        ↓
Transport → Segment
        ↓
Network → Packet
        ↓
Data Link → Frame
        ↓
Physical → Bits
```

At the receiving device, the reverse process (**decapsulation**) removes the headers layer by layer until the original data reaches the application.

---

## 6. Example: Opening a Website

When you visit **https://www.example.com**:

1. **Application Layer** creates an HTTPS request.
2. **Presentation Layer** encrypts the data.
3. **Session Layer** manages the communication session.
4. **Transport Layer** uses TCP to establish a reliable connection and divide data into segments.
5. **Network Layer** adds source and destination IP addresses.
6. **Data Link Layer** adds source and destination MAC addresses.
7. **Physical Layer** transmits the data as electrical, optical, or radio signals.

---

## 7. Cybersecurity Relevance

Understanding the OSI model helps cybersecurity professionals identify where attacks occur and apply appropriate security controls.

| Layer | Example Attack |
|--------|----------------|
| Application | SQL Injection, HTTP attacks |
| Transport | TCP SYN Flood |
| Network | IP Spoofing |
| Data Link | ARP Spoofing, MAC Flooding |
| Physical | Cable Tampering |

SOC analysts use the OSI model to troubleshoot network issues, analyze traffic, investigate attacks, and identify the affected layer during security incidents.

---

## 8. Key Takeaways

- The OSI model divides network communication into seven layers.
- Each layer performs a specific function.
- Data is encapsulated when transmitted and decapsulated when received.
- The OSI model is mainly used for learning, designing, and troubleshooting networks.
- Understanding the OSI model is essential for networking and cybersecurity.
