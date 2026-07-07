# UDP (User Datagram Protocol)

## 1. What is UDP?

**UDP (User Datagram Protocol)** is a **Transport Layer (OSI Layer 4)** protocol that provides **connectionless, best-effort communication** between devices.

It sends data without establishing a connection and does **not** guarantee:
- Delivery
- Ordering
- Retransmission

---

## 2. Why Do We Need UDP?

Not all applications require reliable communication. For many real-time applications, **speed is more important than perfect delivery**.

UDP is commonly used for:
- Live video streaming
- Voice over IP (VoIP)
- Online gaming
- DNS queries

---

## 3. How UDP Works

1. The application creates data.
2. UDP adds a small header to create a **UDP datagram**.
3. IP sends the datagram to the destination.
4. The receiver processes the received data.

Unlike TCP, UDP does **not** establish a connection before sending data.

```text
Application
     │
UDP Datagram
     │
IP
     │
Network
     │
Receiver
```

---

## 4. Features of UDP

- Connectionless communication
- Fast data transmission
- Low overhead
- No acknowledgments
- No retransmissions
- No guaranteed delivery or packet ordering

---

## 5. Advantages

- Very fast communication
- Minimal protocol overhead
- Suitable for real-time applications
- Efficient when occasional packet loss is acceptable

---

## 6. Disadvantages

- No guaranteed delivery
- No acknowledgment mechanism
- No retransmission of lost packets
- No guaranteed packet ordering

---

## 7. Common Applications

UDP is commonly used by:

- DNS
- DHCP
- TFTP
- SNMP
- NTP
- Video streaming
- Voice over IP (VoIP)
- Online gaming

> **Note:** Common port numbers are covered separately in **Common-Ports.md**.

---

## 8. TCP vs UDP

| Feature | TCP | UDP |
|---------|-----|-----|
| Connection | Connection-oriented | Connectionless |
| Reliability | Reliable | Best effort |
| Handshake | Three-way handshake | None |
| Acknowledgments | Yes | No |
| Retransmission | Yes | No |
| Packet Ordering | Guaranteed | Not guaranteed |
| Speed | Slower | Faster |

---

## 9. Cybersecurity Relevance

Understanding UDP is important because:

- DNS and DHCP commonly use UDP.
- SOC analysts investigate unusual UDP traffic.
- Attackers may perform UDP flood attacks.
- Packet analysis tools such as Wireshark capture and analyze UDP traffic.

---

## 10. Key Takeaways

- UDP is a Transport Layer protocol.
- It provides fast, connectionless communication.
- It does not guarantee delivery or packet ordering.
- UDP is ideal for real-time applications where speed is more important than reliability.
