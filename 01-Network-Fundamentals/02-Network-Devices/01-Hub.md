# Hub

## What is a Hub?

A hub is a **Layer 1 (Physical Layer)** network device that connects multiple devices within a **Local Area Network (LAN)**. It receives electrical signals from one port and broadcasts them to all other connected ports without examining the data.

---

## How Does a Hub Work?

Suppose **PC1**, **PC2**, and **PC3** are connected to a hub.

1. PC1 creates an Ethernet frame containing the **source** and **destination MAC addresses**.
2. PC1 sends the frame as electrical signals to the hub.
3. The hub receives the electrical signals and regenerates them before sending the signals out through all other ports.
4. Every connected device receives the frame.
5. Each device's Network Interface Card (NIC) checks the destination MAC address.
6. The intended device recognizes its own MAC address and accepts the frame, while all other devices discard it.

---

## Diagram

```text
                    Hub
             +---------------+
 PC1 --------|               |-------- PC2
             |               |
             |               |-------- PC3
             +---------------+

PC1 sends a frame to PC2

                Broadcast

           ┌────────► PC2 (Accept)
PC1 ─────► Hub
           └────────► PC3 (Discard)
```

---

## Characteristics

- Operates at **OSI Layer 1 (Physical Layer)**.
- Connects multiple devices within a LAN.
- Does not understand **MAC addresses** or **IP addresses**.
- Broadcasts incoming signals to all connected ports.
- Shares the available bandwidth among all connected devices.
- Operates in **half-duplex** mode.
- Creates a **single collision domain**.

---

## Common Uses

Historically, hubs were used to connect multiple devices in small Local Area Networks (LANs). Today, they are rarely used because switches provide better performance, reduce collisions, and improve network security.

---

## Limitations

- Cannot filter network traffic.
- Does not learn MAC addresses.
- Does not reduce network congestion.
- Cannot provide security features.
- Rarely used in modern enterprise networks.

---

## Advantages

- Simple to use.
- Low cost.
- Easy to install.
- Suitable for small or temporary networks (historically).

---

## Disadvantages

- Broadcasts data to all connected devices, creating unnecessary network traffic.
- Slower than a switch.
- Less secure because every connected device receives every frame.
- More collisions occur when multiple devices transmit data at the same time.
- Rarely used in modern networks.

---

## Real-World Example

Imagine a classroom where a teacher reads every student's private letter aloud to the entire class. Everyone hears the message, but only the intended student pays attention to it.

A hub works in a similar way by sending every incoming frame to all connected devices.

---

## Cybersecurity Relevance

Understanding hubs helps cybersecurity professionals learn how Ethernet communication works. Since a hub broadcasts every frame to all connected devices, it makes packet sniffing and eavesdropping easy. This demonstrates why modern networks use switches instead of hubs for better performance, improved security, and reduced network traffic.

---

## Key Takeaways

- A hub is a **Layer 1 (Physical Layer)** network device.
- It broadcasts incoming data to all connected devices.
- It does not use or understand MAC addresses or IP addresses.
- All connected devices share the same bandwidth and collision domain.
- Hubs are rarely used today because switches are faster, more efficient, and more secure.
