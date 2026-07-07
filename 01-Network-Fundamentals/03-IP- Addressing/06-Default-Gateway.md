# Default Gateway

## 1. What is a Default Gateway?

A **default gateway** is the **IP address of a router (or another Layer 3 device)** that a host uses to send packets to destinations outside its local network.

It acts as the **exit point** from the local network to other networks, including the Internet.

---

## 2. Why Do We Need a Default Gateway?

A device can communicate directly only with devices on the same local network.

When the destination is on a different network, the device sends the packet to the **default gateway**, which forwards it to the correct destination.

### Example

**Device Configuration**

- **IP Address:** `192.168.1.10`
- **Subnet Mask:** `255.255.255.0`
- **Default Gateway:** `192.168.1.1`

**Communication**

- Destination: `192.168.1.20` → Same network → Packet is sent directly.
- Destination: `8.8.8.8` → Different network → Packet is sent to the default gateway.

---

## 3. Functions

- Connects the local network to other networks.
- Acts as the exit point for traffic leaving the local network.
- Forwards packets to the appropriate network using its routing table.
- Enables communication with remote networks and the Internet.

---

## 4. Real-World Example

Imagine you live in a neighborhood.

- **Houses** represent devices on your local network.
- **Roads outside the neighborhood** represent other networks.
- The **default gateway** is like the main exit road.

If you visit a neighbor on the same street, you do not need the exit road.

If you travel to another city, you first use the main exit road to leave your neighborhood.

---

## 5. Diagram

```text
             Internet
                 │
          Router (Default Gateway)
             192.168.1.1
                 │
      ┌──────────┼──────────┐
      │          │          │
 Laptop      Phone      Printer
192.168.1.10 192.168.1.20 192.168.1.30
```

---

## 6. Cybersecurity Relevance

Understanding the default gateway is important because:

- Most network traffic passes through it.
- Firewalls are often deployed at or near the gateway.
- SOC analysts monitor traffic entering and leaving the network through the gateway.
- Attackers may target the gateway using techniques such as ARP spoofing or man-in-the-middle attacks.

---

## 7. Key Takeaways

- A default gateway is usually the IP address of a router.
- It is used only when the destination is outside the local network.
- Without a default gateway, devices can communicate only with devices on the same local network.
- The default gateway enables communication with other networks and the Internet.
