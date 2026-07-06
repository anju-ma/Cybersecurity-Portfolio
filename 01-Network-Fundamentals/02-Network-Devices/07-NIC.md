# Network Interface Card (NIC)

## What is a NIC?

A **Network Interface Card (NIC)** is a hardware component that enables a device to connect to a network and communicate with other devices. Every device that communicates over a network, such as a computer, laptop, smartphone, or server, requires a network interface.

---

## Types of NIC

### Wired NIC

A wired NIC connects a device to a network using an **Ethernet cable (RJ-45)**.

### Wireless NIC

A wireless NIC connects a device to a network using **Wi-Fi (IEEE 802.11)** without requiring a physical cable.

---

## How Does a NIC Work?

1. The computer creates data to send over the network.
2. The NIC adds the source and destination **MAC addresses** to create an Ethernet frame.
3. The NIC converts the frame into electrical signals (wired) or radio waves (wireless).
4. The signals are transmitted through the network.
5. When receiving data, the NIC converts the incoming signals back into data.
6. The NIC checks the destination MAC address. If it matches its own MAC address, it accepts the frame; otherwise, it discards it.

---

## Characteristics

- Connects a device to a network.
- Has a unique **MAC address**.
- Can be wired or wireless.
- Sends and receives network data.
- Converts data into network signals and vice versa.

---

## Functions

- Connects the device to a network.
- Sends and receives network data.
- Converts data into electrical or wireless signals.
- Stores a unique MAC address.
- Checks destination MAC addresses before accepting frames.

---

## Advantages

- Enables network communication.
- Supports both wired and wireless connectivity.
- Provides a unique hardware address (MAC address).
- Required for Internet and LAN access.

---

## Disadvantages

- A device cannot communicate over a network without a NIC.
- Hardware failure prevents network connectivity.
- Wired NICs require physical cables.

---

## Real-World Example

A laptop connects to a home Wi-Fi router using its wireless NIC. A desktop computer connects to the same router using its wired Ethernet NIC. Both devices use their NICs to communicate over the network and access the Internet.

---

## Cybersecurity Relevance

NICs are important in cybersecurity because:

- Every network packet enters and leaves through a NIC.
- Packet capture tools such as **Wireshark** capture traffic from a NIC.
- MAC addresses used in investigations belong to NICs.
- Attackers may perform **MAC spoofing**, where they change a NIC's MAC address to impersonate another device.
- Understanding NICs helps SOC analysts analyze network traffic and troubleshoot connectivity issues.

---

## Key Takeaways

- A NIC enables a device to connect to a network.
- Every NIC has a unique MAC address.
- NICs can be wired or wireless.
- NICs send and receive network data.
- NICs are essential for network communication and cybersecurity investigations.
