# IP Addressing

## What is IP Addressing?

**IP addressing** is the process of assigning a unique **Internet Protocol (IP) address** to each device on a network so that devices can be identified and communicate with each other.

---

## What is an IP Address?

An **IP address** is a **logical address** assigned to a device connected to an IP network. It identifies a device on the network and enables data to be sent to the correct destination.

Unlike a **MAC address**, which identifies a device on a local network, an **IP address** is used for communication between different networks.

---

## Why Do We Need IP Addresses?

Imagine there are 100 devices connected to the same network.

Without IP addresses:

- The network would not know which device should receive the data.
- Routers would not be able to forward data between networks.
- Communication over the Internet would not be possible.

IP addresses ensure that data reaches the correct destination.

---

## How Are IP Addresses Assigned?

There are two common methods of assigning IP addresses.

### Static IP Address

A **Static IP Address** is assigned manually and does not change.

It is commonly used for:

- Servers
- Printers
- Routers
- Network devices

### Dynamic IP Address

A **Dynamic IP Address** is assigned automatically by a **DHCP (Dynamic Host Configuration Protocol)** server.

It is commonly used for:

- Laptops
- Smartphones
- Tablets
- Home computers

---

## IP Versions

The two main versions of the Internet Protocol are:

- **IPv4**
- **IPv6**

These are explained in separate notes.

---

## Characteristics

- A logical address assigned to a device.
- Identifies devices on an IP network.
- Used by routers to forward packets between networks.
- Can be static or dynamic.
- Available in IPv4 and IPv6 formats.

---

## Diagram

```text
                Internet
                    │
                 Router
                    │
        ┌───────────┼───────────┐
        │           │           │
 Laptop        Smartphone    Printer
192.168.1.10  192.168.1.20  192.168.1.30
```

Each device has its own IP address, allowing the router to deliver data to the correct destination.

---

## Advantages

- Uniquely identifies devices within an IP network.
- Enables communication between devices and networks.
- Allows routers to forward data correctly.
- Supports Internet communication.
- Makes network management easier.

---

## Disadvantages

- Incorrect IP configuration can prevent communication.
- IP address conflicts can occur if duplicate addresses are assigned.
- Public IP addresses can be targeted by attackers if not properly secured.
- IPv4 addresses are limited, leading to the adoption of IPv6.

---

## Real-World Example

Imagine sending a parcel through the postal service.

- **IP Address** → The destination house address.
- **Router** → The postal sorting office that forwards the parcel.
- **Data Packet** → The parcel.

Without the correct address, the parcel cannot reach its destination.

---

## Cybersecurity Relevance

IP addressing is essential in cybersecurity because security professionals use IP addresses to:

- Identify devices on a network.
- Analyze network traffic.
- Investigate cyber attacks.
- Configure firewall rules.
- Detect suspicious activity.
- Track the source and destination of network connections.

---

## Key Takeaways

- An IP address is a logical address assigned to a device.
- IP addressing allows devices to communicate across networks.
- Routers use IP addresses to forward packets.
- IP addresses can be assigned statically or dynamically.
- The two main IP versions are IPv4 and IPv6.
