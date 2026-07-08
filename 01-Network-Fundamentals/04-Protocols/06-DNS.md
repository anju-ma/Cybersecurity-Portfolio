# Domain Name System (DNS)

## 1. What is DNS?

**DNS (Domain Name System)** is a distributed database system and protocol used to translate human-readable domain names into IP addresses.

In simple terms:

DNS converts domain names into IP addresses that computers use for communication.

Example:

Humans remember:

```
www.google.com
```

Computers communicate using:

```
142.250.195.14
```

DNS performs this translation.

---

## 2. Why Do We Need DNS?

Computers communicate using IP addresses, but remembering IP addresses for every website would be difficult.

Instead of remembering:

```
142.250.195.14
151.101.1.69
104.18.32.47
```

Users can remember:

```
google.com
github.com
example.com
```

DNS acts like the phonebook of the Internet.

---

## 3. How DNS Works (Overview)

When a user enters a domain name:

```
www.example.com
```

The system performs a DNS lookup to find the corresponding IP address.

Basic process:

```
User
 |
Browser
 |
DNS Resolver
 |
DNS Server
 |
IP Address Returned
 |
Web Server
```

After receiving the IP address, the browser connects to the destination server.

(Detailed DNS resolution is covered in Web Fundamentals.)

---

## 4. Types of DNS Servers

### 1. DNS Resolver

The first DNS server contacted by a device.

Responsibilities:

- Receives DNS queries.
- Finds the requested IP address.
- Returns the response to the client.

Examples:

Google DNS:

```
8.8.8.8
```

Cloudflare DNS:

```
1.1.1.1
```

---

### 2. Root DNS Server

The highest level of DNS hierarchy.

It directs queries to the correct Top-Level Domain (TLD) server.

Examples:

```
.com
.org
.net
```

---

### 3. TLD (Top-Level Domain) Server

Manages domains under a specific extension.

Examples:

```
.com
.in
.org
```

---

### 4. Authoritative DNS Server

Contains the actual DNS records for a domain.

Example:

```
example.com → IP address
```

---

## 5. Common DNS Records

| Record | Purpose |
|---|---|
| A | Maps domain name to IPv4 address |
| AAAA | Maps domain name to IPv6 address |
| CNAME | Creates an alias for another domain |
| MX | Specifies mail servers |
| NS | Identifies authoritative DNS servers |
| TXT | Stores text information such as SPF, DKIM, and domain verification data |

---

## 6. DNS Port Usage

DNS commonly uses **port 53** for communication.

- UDP Port 53 → Used for normal DNS queries and responses.
- TCP Port 53 → Used for large DNS responses and DNS zone transfers.

(Detailed explanation of ports is covered in the Ports and Protocols section.)
---

## 7. DNS Cache

DNS cache stores previously resolved domain names and IP addresses.

Example:

```
google.com → 142.250.195.14
```

Benefits:

- Faster DNS lookups
- Reduces DNS traffic

---

## 8. Advantages of DNS

- Makes the Internet easier to use.
- Removes the need to remember IP addresses.
- Improves browsing speed through caching.
- Allows websites to change servers without changing domain names.

---

## 9. Limitations

- DNS can be targeted by attackers.
- Incorrect DNS records can redirect users.
- DNS availability is important for Internet access.

---

## 10. Cybersecurity Relevance

DNS is important in cybersecurity because attackers often abuse DNS for:

- DNS spoofing
- DNS cache poisoning
- DNS tunneling
- Malicious domain communication

Security teams analyze DNS activity to identify suspicious domains and possible malware communication.

---

## 11. Key Takeaways

- DNS translates domain names into IP addresses.
- DNS is essential for Internet communication.
- DNS uses port 53.
- DNS records store different types of information about domains.
- DNS caching improves performance.
- Attackers can abuse DNS for redirection and hidden communication.
