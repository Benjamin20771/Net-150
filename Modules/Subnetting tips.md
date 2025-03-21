# Complete Guide to Subnetting 

![image](https://github.com/user-attachments/assets/772af3e0-ee63-41af-8eb0-63007cf1b96b)

![image](https://github.com/user-attachments/assets/9c0782d3-6219-4cf8-938e-fc9de367507a)


# Midterm quick notes

ipconfig

ipconfig/all

Filter for ICMP (Ping) Packets

In the Wireshark filter bar, enter:
icmp
This filters the packet list to show only ping requests (ICMP Echo Request) and ping replies (ICMP Echo Reply).
Find the Ping Requests:

Click on an ICMP Echo Request packet.
Expand the Ethernet II section in the packet details pane (middle pane).
Locate the Source MAC Address (xx:xx:xx:xx:xx:xx format).
Locate the Destination MAC Address.
Find the Ping Replies:

Click on an ICMP Echo Reply packet.
Expand the Internet Protocol (IP) section.
Locate the Source IP Address (this is the sender of the reply).
Locate the Destination IP Address (this is the original sender of the ping request).

Answering Your Questions:
Source MAC Address of Ping Requests → Found in the Ethernet II section under Source.
Destination MAC Address of Ping Requests → Found in the Ethernet II section under Destination.
Source IP Address of the Ping Reply → Found in the IP Header under Source.
Destination IP Address of the Ping Reply → Found in the IP Header under Destination.

# IPV4 summary

192.168.X.Z

X is the Network Address assigned to a network. All IPV4 addresses will have the same network address (X).

Z is the Host Address. Each IPV4 address will have a different one in the network. 

X is the unique identifier for networks while Z is the unique identifier for each device in the network

# Subent Mask

A subnet mask masks the network portion of an IP address to reveal how many bits are used in the network.

# Example

## IP Addressing Scheme:

### LAN 1 (connected to Router1):

Network Address: 192.168.1.0/24

Router1 LAN Interface: 192.168.1.1

PC1: 192.168.1.2

PC2: 192.168.1.3

PC3: 192.168.1.4

PC4: 192.168.1.5

### LAN 2 (connected to Router2):

Network Address: 192.168.2.0/24

Router2 LAN Interface: 192.168.2.1

PC5: 192.168.2.2

PC6: 192.168.2.3

PC7: 192.168.2.4 

## Inter-Router Connection:

Network Address: 10.0.0.0/30

Router1 Serial Interface: 10.0.0.1

Router2 Serial Interface: 10.0.0.2

## Configuration Steps:

Assign IP Addresses:

### Router1:

LAN Interface (connected to Switch1): 192.168.1.1/24

Serial Interface (connected to Router2): 10.0.0.1/30

### Router2:

LAN Interface (connected to Switch2): 192.168.2.1/24

Serial Interface (connected to Router1): 10.0.0.2/30

### PCs:

Assign IP addresses as per the scheme above.

Set the default gateway of PCs in LAN 1 to 192.168.1.1.

Set the default gateway of PCs in LAN 2 to 192.168.2.1.

## Configure Routing:

### Router1:

Add a static route to LAN 2:

ip route 192.168.2.0 255.255.255.0 10.0.0.2

### Router2:

Add a static route to LAN 1:

ip route 192.168.1.0 255.255.255.0 10.0.0.1

## Connect Devices:

### Switch1:

Connect to Router1's LAN interface.

Connect PC1, PC2, PC3, and PC4 to Switch1.

### Switch2:

Connect to Router2's LAN interface.

Connect PC5, PC6, and PC7 to Switch2.

### Inter-Router Link:

Connect Router1's serial interface to Router2's serial interface.
