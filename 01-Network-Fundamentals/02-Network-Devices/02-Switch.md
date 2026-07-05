# Switch

## What is a Switch?

A switch is a **Layer 2 (Data Link Layer)** network device that connects multiple devices within a **Local Area Network (LAN)**. It forwards Ethernet frames only to the intended destination device by using **MAC addresses**.

---

## How Does a Switch Work?

Suppose **PC1** wants to send data to **PC2**.

1. PC1 creates an Ethernet frame containing the **source** and **destination MAC addresses**.
2. The Network Interface Card (NIC) converts the frame into electrical signals and sends it to the switch.
3. The switch receives the frame and examines the destination MAC address.
4. The switch checks its **MAC Address Table (MAC Table)**.
5. If the destination MAC address exists in the MAC Address Table, the switch forwards the frame only to the corresponding port.
6. If the destination MAC address is unknown, the switch floods the frame to all ports except the incoming port. Once the destination device replies, the switch learns its MAC address and updates the MAC Address Table.

---

## Diagram

```text
                    Switch
              +----------------+
 PC1 ---------|                |-------- PC2 ✓
 PC3 ---------|                |
              +----------------+

PC1 sends data to PC2

Switch checks the MAC Address Table

Forward only to PC2
```

---

## Characteristics

- Operates at **OSI Layer 2 (Data Link Layer)**.
- Connects multiple devices within a LAN.
- Learns MAC addresses automatically.
- Maintains a **MAC Address Table**.
- Reads the destination MAC address.
- Forwards frames only to the correct destination port.
- Reduces unnecessary network traffic.
- Supports **full-duplex** communication (devices can send and receive simultaneously).
- Creates a separate **collision domain** for each port.

---

## Switch Ports

A switch contains multiple physical ports used to connect network devices such as computers, printers, servers, and access points. Each port represents a separate collision domain, allowing devices to communicate independently and reducing collisions.

---

## MAC Address Table

A **MAC Address Table** stores the MAC addresses of connected devices along with the switch port on which each device is connected. The switch learns these addresses automatically from incoming frames and uses the table to forward frames only to the correct destination port.

---

## Unknown Destination MAC Address

If the destination MAC address is not found in the MAC Address Table, the switch floods the frame to all ports except the incoming port. When the destination device replies, the switch learns its MAC address and updates the MAC Address Table for future communication.

---

## Collision Domain

Each switch port creates a separate **collision domain**. This reduces collisions and improves network performance compared to a hub, where all devices share the same collision domain.

---

## Advantages

- Faster than a hub.
- More secure than a hub.
- Reduces unnecessary network traffic.
- Makes efficient use of available bandwidth.
- Supports many connected devices.
- Minimizes collisions.
- Supports full-duplex communication.

---

## Disadvantages

- More expensive than a hub.
- Slightly more complex to configure and manage.
- Can be vulnerable to attacks such as **MAC flooding** if not properly secured.

---

## Hub vs Switch

| Hub | Switch |
|------|---------|
| Operates at Layer 1 | Operates at Layer 2 |
| Broadcasts frames to all ports | Forwards frames only to the destination port |
| Does not learn MAC addresses | Learns MAC addresses automatically |
| Half-duplex | Full-duplex |
| Single collision domain | Separate collision domain for each port |
| Less secure | More secure |
| Slower | Faster |

---

## Real-World Example

A switch is like a postal worker who reads the address on an envelope and delivers it only to the correct house instead of delivering copies to every house in the neighborhood.

---

## Cybersecurity Relevance

Understanding switches is important for cybersecurity because:

- Most modern networks use switches.
- SOC analysts monitor and analyze traffic flowing through switched networks.
- Switches help reduce unnecessary network traffic, making monitoring more efficient.
- Attackers may target switches using attacks such as **MAC flooding**.
- Understanding switches is essential when learning **ARP**, **VLANs**, **packet forwarding**, and **network segmentation**.

---

## Key Takeaways

- A switch is a **Layer 2 (Data Link Layer)** network device.
- It connects multiple devices within a Local Area Network (LAN).
- It learns and stores MAC addresses in a **MAC Address Table**.
- It forwards frames only to the intended destination device.
- Each switch port creates a separate collision domain, reducing collisions.
- Switches are faster, more efficient, and more secure than hubs.
