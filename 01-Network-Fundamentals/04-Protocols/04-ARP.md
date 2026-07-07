# Address Resolution Protocol (ARP)

## 1. What is ARP?

**ARP (Address Resolution Protocol)** is a network protocol used to find the **MAC address** of a device when its **IPv4 address** is known.

In simple terms, ARP maps an **IPv4 address** to a **MAC address** on a Local Area Network (LAN).

---

## 2. Why Do We Need ARP?

Devices communicate over a LAN using **MAC addresses**, while applications and users typically identify devices using **IP addresses**.

When a device knows the destination IP address but not the corresponding MAC address, it uses **ARP** to discover the MAC address before sending data.

---

## 3. Where Is ARP Used?

ARP is used **only within a Local Area Network (LAN).**

If the destination device is on another network, the sender first resolves the **MAC address of the default gateway**, which then forwards the packet to the destination network.

---

## 4. How ARP Works

Suppose **PC1 (192.168.1.10)** wants to communicate with **PC2 (192.168.1.20)**.

### Step 1 – Check the ARP Cache

PC1 checks its ARP cache to see if it already knows the MAC address of **192.168.1.20**.

If an entry exists, it sends the data immediately.

If not, it proceeds to the next step.

---

### Step 2 – Send an ARP Request

PC1 sends a **broadcast** message to every device on the local network.

> "Who has IP address **192.168.1.20**? Tell **192.168.1.10**."

The destination MAC address of the Ethernet frame is:

```
FF:FF:FF:FF:FF:FF
```

---

### Step 3 – Receive the ARP Reply

Only the device with IP address **192.168.1.20** replies.

It sends a **unicast** message back to PC1 containing its MAC address.

---

### Step 4 – Update the ARP Cache

PC1 stores the IP-to-MAC mapping in its ARP cache for future communication.

Example:

| IP Address | MAC Address |
|------------|-------------|
| 192.168.1.20 | BB:BB:BB:BB:BB:BB |

---

### Step 5 – Send the Data

PC1 now creates an Ethernet frame using the discovered MAC address, and the switch forwards the frame directly to PC2.

---

## 5. ARP Request vs ARP Reply

| ARP Request | ARP Reply |
|-------------|-----------|
| Broadcast | Unicast |
| Sent to all devices on the LAN | Sent only to the requesting device |
| Asks for a MAC address | Returns the MAC address |

---

## 6. ARP Cache

The **ARP cache** is a temporary table that stores IP-to-MAC address mappings.

It helps reduce network traffic by avoiding repeated ARP requests for devices that have already been discovered.

---

## 7. ARP Packet Fields

An ARP message contains:

- Hardware Type
- Protocol Type
- Hardware Address Length
- Protocol Address Length
- Operation (Request or Reply)
- Sender MAC Address
- Sender IP Address
- Target MAC Address
- Target IP Address

---

## 8. Limitations

- Works only within a Local Area Network (LAN).
- Broadcast requests generate additional network traffic.
- Vulnerable to ARP spoofing attacks.

---

## 9. Cybersecurity Relevance

ARP is important in cybersecurity because attackers can exploit it through **ARP Spoofing (ARP Poisoning)**.

In an ARP spoofing attack, an attacker sends fake ARP replies so that victims associate the attacker's MAC address with another IP address (often the default gateway).

This can lead to:

- Man-in-the-Middle (MITM) attacks
- Traffic interception
- Session hijacking
- Denial of Service (DoS)

SOC analysts and digital forensics investigators often examine ARP tables and ARP traffic when investigating local network attacks.

---

## 10. Key Takeaways

- ARP maps an IPv4 address to a MAC address.
- ARP operates only within a Local Area Network (LAN).
- ARP Request is a broadcast message.
- ARP Reply is a unicast message.
- Devices store IP-to-MAC mappings in an ARP cache.
- ARP is essential for IPv4 communication over Ethernet.
- ARP spoofing is a common local network attack.
