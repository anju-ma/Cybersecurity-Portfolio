# TCP (Transmission Control Protocol)

## 1. What is TCP?

**TCP (Transmission Control Protocol)** is a **Transport Layer (OSI Layer 4)** protocol that provides **reliable, connection-oriented communication** between devices on an IP network.

It ensures that:
- Data is delivered reliably.
- Data arrives in the correct order.
- Lost data is retransmitted.
- Errors are detected during transmission.

---

## 2. Why Do We Need TCP?

Large files and messages are divided into smaller pieces called **segments** before transmission.

TCP ensures that:
- All segments reach the destination.
- Segments are reassembled in the correct order.
- Lost segments are retransmitted.
- Duplicate segments are discarded.

Without TCP, data could be lost, arrive out of order, or become corrupted.

---

## 3. How TCP Works

### 1. Connection Establishment (Three-Way Handshake)

Before data transfer begins, TCP establishes a connection.

```text
Client                 Server

SYN  -------------------->
      <------------------- SYN-ACK
ACK  -------------------->
```

---

### 2. Data Transfer

- Data is divided into TCP segments.
- Each segment is assigned a sequence number.
- The receiver sends acknowledgments (ACKs) after receiving data.
- If an acknowledgment is not received, TCP retransmits the lost segment.

---

### 3. Connection Termination

After communication is complete, TCP closes the connection using a **four-way handshake**.

---

## 4. Features of TCP

- Connection-oriented communication
- Reliable data delivery
- Ordered delivery
- Error detection using checksums
- Flow control
- Congestion control

---

## 5. Advantages

- Reliable communication
- Detects transmission errors
- Ensures ordered delivery
- Retransmits lost data
- Suitable for applications requiring data integrity

---

## 6. Disadvantages

- Higher overhead than UDP
- Slower because of acknowledgments and connection management
- Not ideal for real-time applications where low latency is more important than reliability

---

## 7. Common Applications

TCP is commonly used by:

- HTTP
- HTTPS
- FTP
- SSH
- SMTP
- POP3
- IMAP

> **Note:** Common port numbers are covered separately in **Common-Ports.md**.

---

## 8. Cybersecurity Relevance

Understanding TCP is important because:

- Most web traffic uses TCP.
- SOC analysts analyze TCP connections in network logs.
- Tools like Wireshark display TCP handshakes, sequence numbers, and TCP flags.
- Port scanning tools such as Nmap commonly scan TCP ports.
- Attacks such as TCP SYN Flood target TCP communication.

---

## 9. Key Takeaways

- TCP is a Transport Layer protocol.
- It provides reliable, connection-oriented communication.
- It ensures ordered delivery and retransmits lost data.
- TCP uses the Three-Way Handshake to establish a connection.
- It is widely used by web, email, file transfer, and remote access protocols.
