## Routing
Routing is the process of forwarding packets between different networks using a router.

Routers operate at Layer 3 (Network Layer) of the OSI model.

### Broadcast Domains & Need for Routing
A broadcast domain is a network segment where a broadcast frame is forwarded.

Routers break up broadcast domains, reducing unnecessary traffic and enhancing performance/security.

### Switching vs. Routing Tables
#### Switching Table (MAC address table):

Used by switches (Layer 2).

Maps MAC addresses to specific ports.

#### Routing Table:

Used by routers (Layer 3).

Contains routes to different networks and next-hop addresses.

### Contents of a Routing Table
Destination network

Subnet mask

Next-hop IP address

Outgoing interface

Metric (optional; indicates route cost)

Route source (e.g., static, RIP)

### Static vs. Dynamic Routing
#### Static Routing:

Manually configured.

Simple and secure but not scalable.

#### Dynamic Routing:

Automatically adjusts routes.

Uses protocols like RIP, OSPF.

Better for large or changing networks.

### Static Routing Config Steps (General)
Identify networks to connect.

Assign IPs to interfaces.

Define static routes (destination, subnet, next-hop).

Test with ping or traceroute.

### Benefits of Dynamic Routing
Automatically adapts to network changes.

Reduces manual configuration.

Scalable for larger networks.

### Routing Protocols
Protocols that enable routers to share routing info (e.g., RIP, OSPF, BGP).

### IGP vs EGP
#### IGP (Interior Gateway Protocol):

Used within an organization.

Examples: RIP, OSPF, EIGRP.

#### EGP (Exterior Gateway Protocol):

Used between organizations.

Example: BGP (Border Gateway Protocol).

### Distance Vector vs. Link State
#### Distance Vector:

Shares the entire routing table with neighbors.

Simple but slower convergence.

Example: RIP.

#### Link State:

Shares info about directly connected links.

Faster and more efficient.

Example: OSPF.

### RIPv2 Overview
A distance vector protocol using hop count.

Max 15 hops; beyond that = unreachable.

Sends updates every 30 seconds.

Supports VLSM and multicast updates.

### RIPv2 Configuration (General)
Enable RIP on a router.

Specify networks to advertise.

Use version 2.

## VLANs
### Definition
VLAN (Virtual LAN): A logical grouping of devices on different physical networks into one broadcast domain.

### Benefits
Improves security and performance.

Segments traffic logically, not just physically.

Reduces broadcast traffic.

### VLANs and Layer 3
VLANs are Layer 2, but communication between them requires a Layer 3 device (router or Layer 3 switch).

### Access vs Trunk Ports
Access Port: Connects to end devices; carries traffic for one VLAN.

Trunk Port: Connects to other switches/routers; carries traffic for multiple VLANs using tagging (802.1Q).

## Wireless Networking
### Benefits
Mobility, flexibility, scalability.

Easy deployment and cost-effective.

### Access Point
A device that connects wireless devices to a wired network.

### SSID
Service Set Identifier – the name of a wireless network.

### Wi-Fi Channels
Frequency subdivisions in 2.4GHz and 5GHz bands.

Use non-overlapping channels (e.g., 1, 6, 11 in 2.4GHz) to avoid interference.

### Wi-Fi Security (WPA2)
WPA2 uses AES encryption and is more secure than WEP or WPA.

WPA2-Enterprise adds authentication with a RADIUS server.
