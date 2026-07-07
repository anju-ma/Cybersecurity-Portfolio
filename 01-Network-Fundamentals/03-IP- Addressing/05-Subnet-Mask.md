## What is a Subnet Mask?

A subnet mask is a **32-bit number** used with an IPv4 address to divide it into:

- Network ID
- Host ID

It helps devices determine whether another device is on the same network or a different network.

---

## Why Do We Need a Subnet Mask?

Without a subnet mask, a device cannot determine whether data should be sent directly to another device or forwarded to a router.

---

## Structure

Example:

IP Address

192.168.1.10

Subnet Mask

255.255.255.0

The first three octets identify the network.

The last octet identifies the host.

---

## Example

PC1

192.168.1.10

PC2

192.168.1.20

Mask

255.255.255.0

Both devices are on the same network because they share the same network portion (192.168.1).

If PC2 had the address 192.168.2.20, it would be on a different network and communication would go through the router.

---

## Common Subnet Masks

| Subnet Mask | CIDR |
|-------------|------|
|255.0.0.0|/8|
|255.255.0.0|/16|
|255.255.255.0|/24|

---

## Advantages

- Separates networks into smaller segments.
- Reduces broadcast traffic.
- Improves network performance.
- Makes IP address allocation more efficient.

---

## Disadvantages

- Incorrect subnet masks can prevent communication.
- Requires planning for large networks.
- Can increase configuration complexity.

---

## Real-World Analogy

Imagine a city.

- **Network ID** = Street name
- **Host ID** = House number

The subnet mask tells you which part is the street and which part is the house number.

---

## Cybersecurity Relevance

Subnet masks are important because they help security professionals:

- Segment networks into security zones.
- Configure routers and firewalls.
- Analyze network traffic.
- Investigate incidents.
- Understand network topology.

---

## Key Takeaways

- A subnet mask is a 32-bit value used with an IPv4 address.
- It divides an IP address into a network portion and a host portion.
- It determines whether devices are on the same network.
- Routers use subnet information to forward traffic between networks.
- Understanding subnet masks is essential for networking and cybersecurity.
