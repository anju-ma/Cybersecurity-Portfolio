# Router

## What is a Router?

A router is a **Layer 3 (Network Layer)** network device that connects two or more different IP networks and forwards data packets between them using **IP addresses**.

---

## Why Do We Need a Router?

A switch connects devices within the same **Local Area Network (LAN)**.

A router is required to:

- Connect a home or office network to the Internet.
- Connect one LAN to another LAN.
- Connect different IP networks.
- Forward packets between different networks.

Without a router, devices on the same LAN can communicate with each other, but they cannot access other networks or the Internet.

---

## How Does a Router Work?

Suppose your laptop wants to open **www.google.com**.

1. You enter **www.google.com** in your web browser.
2. The computer creates an **IP packet** containing:
   - Source IP Address: `192.168.1.10`
   - Destination IP Address: Google's server
3. The packet is sent to the **default gateway (router)**.
4. The router receives the packet and examines the **destination IP address**.
5. The router checks its **Routing Table** to determine the best path.
6. The router forwards the packet to the next network, usually the **Internet Service Provider (ISP)**.
7. The packet travels across the Internet until it reaches the destination server.

---

## Diagram

```text
              Home Network

 Laptop (192.168.1.10)
           │
           │
 Default Gateway
 Router (192.168.1.1)
           │
           │
          ISP
           │
       Internet
           │
   Google Server
```

---

## Characteristics

- Operates at **OSI Layer 3 (Network Layer)**.
- Connects different IP networks.
- Uses **IP addresses** to forward packets.
- Maintains a **Routing Table**.
- Chooses the best path for forwarding packets.
- Separates **broadcast domains**.
- Can perform **Network Address Translation (NAT)**.
- Often provides **DHCP** and **basic firewall** functionality.

---

## Routing Table

A **Routing Table** is a database maintained by a router that stores information about available networks and the best path to reach them.

Example:

| Destination Network | Next Hop |
|---------------------|----------|
| 192.168.1.0/24 | Local LAN |
| Default Route | ISP |

The router checks this table before forwarding every packet.

---

## Default Gateway

A **default gateway** is the IP address of the router that a device uses to send data to another network or the Internet.

Example:

- Laptop IP Address: **192.168.1.10**
- Default Gateway: **192.168.1.1**

When the destination is outside the local network, the laptop sends the packet to the default gateway.

---

## Home Router

A typical home Wi-Fi router combines several networking devices into one device:

- Router
- Switch
- Wireless Access Point (Wi-Fi)
- DHCP Server
- NAT
- Basic Firewall

Because of this, a home router can:

- Assign IP addresses to devices.
- Connect wired devices.
- Provide Wi-Fi connectivity.
- Connect the home network to the Internet.
- Provide basic network security.

---

## Router vs Switch

| Feature | Switch | Router |
|----------|---------|---------|
| OSI Layer | Layer 2 | Layer 3 |
| Uses | MAC Address | IP Address |
| Connects | Devices within a LAN | Different Networks |
| Forwards | Ethernet Frames | IP Packets |
| Broadcast Domain | Same Broadcast Domain | Separates Broadcast Domains |
| Internet Access | No | Yes |

---

## Advantages

- Connects multiple networks.
- Provides Internet access.
- Chooses efficient paths for data.
- Supports communication between different IP networks.
- Can improve security using NAT and firewall features.
- Reduces unnecessary broadcast traffic between networks.

---

## Disadvantages

- More expensive than a switch.
- More complex to configure and manage.
- Can become a bottleneck if overloaded.
- Requires proper configuration for secure operation.

---

## Real-World Example

Imagine a postal system.

A **switch** is like a receptionist delivering letters to rooms within the same office building.

A **router** is like a post office that sends letters from one city to another.

Similarly, a router forwards data between different networks.

---

## Cybersecurity Relevance

Routers are important in cybersecurity because they:

- Control traffic entering and leaving a network.
- Can filter traffic using firewall rules.
- Hide private IP addresses using **Network Address Translation (NAT)**.
- Generate logs useful for monitoring and incident response.
- Are common targets for attackers if left unsecured.
- Help security professionals understand routing, packet forwarding, NAT, and network segmentation.

---

## Key Takeaways

- A router is a **Layer 3 (Network Layer)** device.
- It connects different IP networks.
- It forwards packets using **IP addresses**.
- It maintains a **Routing Table** to choose the best path.
- It separates broadcast domains.
- Home routers usually include a switch, Wi-Fi access point, DHCP server, NAT, and firewall.
