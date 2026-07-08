# Port

## 1. What is a Port?

A **port** is a logical communication endpoint used by the **Transport Layer (TCP and UDP)** to identify a specific application or service running on a device.

In simple terms:

- **IP address identifies the device.**
- **Port number identifies the application or service on that device.**

Example:

```
IP Address:
192.168.1.10

Port:
443

Service:
HTTPS
```

---

## 2. Why Do We Need Ports?

A computer can run multiple network applications at the same time.

Example:

- Web browser
- Email application
- SSH service
- Video calling application

All applications use the same IP address.

The operating system uses port numbers to determine which application should receive incoming data.

Without ports, a device would not know which application should process received network traffic.

---

## 3. Real-World Analogy

Imagine an apartment building.

```
IP Address = Building Address

Port Number = Apartment Number
```

Example:

```
123 Main Street

Apartment 101 → Web Server
Apartment 102 → Email Server
Apartment 103 → SSH Server
```

The address identifies the building, and the apartment number identifies the correct destination.

Similarly:

```
IP Address → Device
Port Number → Application/Service
```

---

## 4. How Does a Port Work?

Suppose a user opens a website.

The browser sends a request:

```
Destination IP:
142.250.xxx.xxx

Destination Port:
443
```

The server receives the packet and checks the destination port.

Because the port is:

```
443
```

the operating system forwards the request to the HTTPS service.

---

## 5. Port Numbers

Port numbers range from:

```
0 - 65535
```

Ports are **16-bit numbers**.

Total available ports:

```
2¹⁶ = 65,536
```

---

# 6. Types of Port Ranges

## 1. Well-Known Ports

Range:

```
0 - 1023
```

Used for common services.

Examples:

| Port | Protocol | Service |
|---|---|---|
| 21 | TCP | FTP |
| 22 | TCP | SSH |
| 23 | TCP | Telnet |
| 25 | TCP | SMTP |
| 53 | TCP/UDP | DNS |
| 80 | TCP | HTTP |
| 443 | TCP | HTTPS |

---

## 2. Registered Ports

Range:

```
1024 - 49151
```

Used by applications and software.

Examples:

| Port | Service |
|---|---|
| 3306 | MySQL |
| 3389 | RDP |

---

## 3. Dynamic/Ephemeral Ports

Range:

```
49152 - 65535
```

Temporary ports automatically assigned by the operating system.

Example:

```
Client:

Source Port:
52341


Server:

Destination Port:
443
```

After communication ends, the temporary port can be reused.

---

# 7. Source Port and Destination Port

TCP and UDP segments contain two port numbers.

## Source Port

Identifies the sending application.

Example:

```
52341
```

## Destination Port

Identifies the receiving service.

Example:

```
443
```

Example communication:

```
Source IP:
192.168.1.10

Source Port:
52341


Destination IP:
142.250.xxx.xxx

Destination Port:
443
```

---

# 8. Open, Closed, and Filtered Ports

## Open Port

A service is actively listening on that port.

Example:

```
Port 80 → Open

Web server is running.
```

---

## Closed Port

No service is listening.

Example:

```
Port 25 → Closed
```

The device responds but no application is using that port.

---

## Filtered Port

A firewall or security device blocks access.

The scanner may receive no response.

---

# 9. Socket

A socket identifies a network connection using:

```
IP Address + Port Number + Protocol
```

Example:

```
192.168.1.10:443/TCP
```

This allows multiple applications to communicate simultaneously.

---

# 10. Advantages of Ports

- Allow multiple applications to use the same IP address.
- Help operating systems deliver data to the correct application.
- Allow network services to be identified.
- Help firewalls control network access.

---

# 11. Cybersecurity Relevance

Ports are important in cybersecurity because attackers often scan ports to discover available services.

Security professionals use port information to:

- Identify running services.
- Find exposed services.
- Verify firewall rules.
- Analyze network traffic.

Common tools:

- **Nmap** → Port scanning and service discovery.
- **Wireshark** → Traffic analysis.

Examples of attacks:

| Port | Service | Common Attack |
|---|---|---|
| 22 | SSH | Brute-force attacks |
| 3389 | RDP | Unauthorized remote access |
| 445 | SMB | Malware and ransomware attacks |

---

# 12. Key Takeaways

- Ports identify applications and services on a device.
- IP addresses identify devices.
- TCP and UDP use port numbers.
- Port numbers range from 0 to 65535.
- Open ports represent available services.
- Attackers scan ports to find possible targets.
- Understanding ports is essential for network security.
