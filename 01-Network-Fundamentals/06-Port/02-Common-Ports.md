# Common Network Ports

## Introduction

Common ports are **well-known port numbers assigned to frequently used network services and protocols**.

A port number helps the operating system identify **which service or application should receive network traffic**.

Example:

```
Destination IP:
192.168.1.50

Destination Port:
443
```

The device understands:

```
This traffic is for the HTTPS service.
```

---

# 1. FTP (File Transfer Protocol)

## Port:

```
TCP 20, TCP 21
```

## Purpose:

Used to transfer files between a client and a server.

- Port 21 → FTP control commands
- Port 20 → File data transfer

## Security Relevance:

FTP sends data, usernames, and passwords in plain text.

Common risks:

- Credential theft
- Packet sniffing

Secure alternatives:

- SFTP
- FTPS

---

# 2. SSH (Secure Shell)

## Port:

```
TCP 22
```

## Purpose:

Provides secure remote access to systems.

Used for:

- Remote administration
- Server management
- Secure file transfer

## Security Relevance:

Common attacks:

- Brute-force login attempts
- Weak authentication

---

# 3. Telnet

## Port:

```
TCP 23
```

## Purpose:

Provides remote command-line access.

## Security Relevance:

Telnet sends data in plain text.

Risks:

- Username exposure
- Password exposure
- Command interception

Secure replacement:

- SSH

---

# 4. SMTP (Simple Mail Transfer Protocol)

## Port:

```
TCP 25
```

## Purpose:

Used for sending emails between mail servers.

## Security Relevance:

Can be abused for:

- Spam
- Email spoofing
- Phishing campaigns

---

# 5. DNS (Domain Name System)

## Ports:

```
UDP 53
TCP 53
```

## Purpose:

Translates domain names into IP addresses.

Example:

```
google.com

↓

142.250.x.x
```

## UDP 53:

Used for normal DNS queries.

## TCP 53:

Used for:

- Large DNS responses
- Zone transfers

## Security Relevance:

Common attacks:

- DNS spoofing
- DNS cache poisoning
- DNS tunneling

---

# 6. DHCP (Dynamic Host Configuration Protocol)

## Ports:

```
UDP 67 - Server
UDP 68 - Client
```

## Purpose:

Automatically assigns network configuration:

- IP address
- Subnet mask
- Default gateway
- DNS server

Example:

When a phone connects to Wi-Fi, DHCP provides network settings.

## Security Relevance:

Attack:

- Rogue DHCP server

Attackers may provide fake:

- Gateway
- DNS server

---

# 7. HTTP (Hypertext Transfer Protocol)

## Port:

```
TCP 80
```

## Purpose:

Used for web communication.

Example:

```
Browser → HTTP Request → Web Server
```

## Security Relevance:

HTTP traffic is not encrypted.

Risks:

- Data interception
- Credential exposure

---

# 8. HTTPS (HTTP Secure)

## Port:

```
TCP 443
```

## Purpose:

Secure version of HTTP.

Uses:

- TLS encryption

Provides:

- Confidentiality
- Integrity
- Authentication

Example:

```
https://bank.com
```

## Security Relevance:

HTTPS protects communication, but websites can still contain vulnerabilities.

---

# 9. POP3 (Post Office Protocol)

## Port:

```
TCP 110
```

## Purpose:

Used to download emails from a mail server.

Secure version:

```
POP3S → TCP 995
```

---

# 10. IMAP (Internet Message Access Protocol)

## Port:

```
TCP 143
```

## Purpose:

Used to access and manage emails while keeping them stored on the server.

Secure version:

```
IMAPS → TCP 993
```

---

# 11. NTP (Network Time Protocol)

## Port:

```
UDP 123
```

## Purpose:

Synchronizes time between network devices.

Important for:

- Accurate logs
- Authentication systems

## Security Relevance:

Attack:

- NTP amplification attack

---

# 12. SNMP (Simple Network Management Protocol)

## Port:

```
UDP 161
```

## Purpose:

Used to monitor and manage network devices.

Examples:

- Routers
- Switches
- Servers

## Security Relevance:

Older SNMP versions may expose information.

Secure version:

- SNMPv3

---

# 13. LDAP (Lightweight Directory Access Protocol)

## Port:

```
TCP/UDP 389
```

## Purpose:

Used for directory services.

Examples:

- User authentication
- User information lookup

Commonly used with:

- Active Directory

Secure version:

```
LDAPS → TCP 636
```

---

# 14. SMB (Server Message Block)

## Port:

```
TCP 445
```

## Purpose:

Used for:

- File sharing
- Printer sharing
- Windows network communication

Example:

```
Computer → Shared Folder
```

## Security Relevance:

Common targets for:

- Malware
- Ransomware
- Lateral movement

---

# 15. RDP (Remote Desktop Protocol)

## Port:

```
TCP 3389
```

## Purpose:

Provides remote graphical access to Windows systems.

Example:

```
Administrator → RDP → Windows Server
```

## Security Relevance:

Common attacks:

- Brute-force attacks
- Credential theft
- Unauthorized access

---

# Common Ports Summary

| Port | Protocol | Service | Purpose |
|---|---|---|---|
| 20/21 | TCP | FTP | File Transfer |
| 22 | TCP | SSH | Secure Remote Access |
| 23 | TCP | Telnet | Remote Access |
| 25 | TCP | SMTP | Email Sending |
| 53 | TCP/UDP | DNS | Name Resolution |
| 67/68 | UDP | DHCP | IP Assignment |
| 80 | TCP | HTTP | Web Communication |
| 110 | TCP | POP3 | Email Retrieval |
| 123 | UDP | NTP | Time Synchronization |
| 143 | TCP | IMAP | Email Access |
| 161 | UDP | SNMP | Network Monitoring |
| 389 | TCP/UDP | LDAP | Directory Services |
| 443 | TCP | HTTPS | Secure Web |
| 445 | TCP | SMB | File Sharing |
| 3389 | TCP | RDP | Remote Desktop |

---

# Cybersecurity Importance of Ports

Security professionals use ports to:

## 1. Identify Services

Example:

```
Port 22 Open

↓

SSH Service Running
```

---

## 2. Find Attack Surface

More exposed ports can mean more possible entry points.

Example:

```
Port 3389 Open

↓

RDP Exposed

↓

Possible Brute-force Attempts
```

---

## 3. Analyze Network Traffic

Network analysis checks:

- Source IP
- Destination IP
- Source Port
- Destination Port
- Protocol

Example:

```
192.168.1.20:52341

↓

8.8.8.8:53 UDP
```

Meaning:

A device is sending a DNS query.

---

## 4. Configure Firewalls

Example:

Allow:

```
TCP 443
```

Block:

```
TCP 23
```

---

# Key Takeaways

- Ports identify services running on a device.
- TCP and UDP use port numbers.
- Port numbers range from 0 to 65535.
- Open ports represent available services.
- Attackers scan ports to discover possible targets.
- Understanding common ports helps in network troubleshooting and security analysis.
