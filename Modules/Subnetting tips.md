# Complete Guide to Subnetting 192.25.10.0/24 into 5 Subnets

### Step 1: Understand the Given Network

Starting Network Address: 192.25.10.0

Default Subnet Mask: /24 (255.255.255.0)

Total Addresses in /24: 256 (0-255)

Hosts Required for Each Subnet:

Foster → 30 hosts

Joyce → 20 hosts

Skiff → 30 hosts

Foster to Skiff → 2 hosts

Joyce to Skiff → 2 hosts

Each subnet will require a subnet mask that provides at least the needed number of usable hosts.

### Step 2: Determine the Required Subnet Sizes
The subnet mask determines how many IPs a subnet has. To find the correct subnet mask, we use the formula:

Total Addresses
=
2
ℎ
Total Addresses=2 
h
 
Usable Hosts
=
2
ℎ
−
2
Usable Hosts=2 
h
 −2
Where:

h is the number of host bits.
Subtracting 2 accounts for the network and broadcast addresses.
We select the smallest power of 2 that fits the required hosts:

Required Hosts	Total Needed (2^h)	Usable Hosts	Subnet Mask (CIDR)

30--32--30--/27=(255.255.255.224)

20--32--30--/27=(255.255.255.224)

30--32--30--/27=(255.255.255.224)

2--4--2--/30=(255.255.255.252)

2--4--2--/30=(255.255.255.252)

### Step 3: Assign Subnet Addresses
We start at 192.25.10.0 and increment by the subnet size.

Subnet	Network Address	Subnet Mask	Total Addresses	Usable Hosts	Broadcast Address

Foster (30 hosts)	192.25.10.0	255.255.255.224 (/27)	32	30	192.25.10.31

Joyce (20 hosts)	192.25.10.32	255.255.255.224 (/27)	32	30	192.25.10.63

Skiff (30 hosts)	192.25.10.64	255.255.255.224 (/27)	32	30	192.25.10.95

Foster to Skiff (2 hosts)	192.25.10.96	255.255.255.252 (/30)	4	2	192.25.10.127

Joyce to Skiff (2 hosts)	192.25.10.100	255.255.255.252 (/30)	4	2	192.25.10.159

### Step 4: Find Usable IP Ranges
Each subnet has:

First usable address: Network address +1

Last usable address: Broadcast address -1

Subnet	Lowest Host	Highest Host

Foster	192.25.10.1--192.25.10.30

Joyce	192.25.10.33--192.25.10.62

Skiff	192.25.10.65--192.25.10.94

Foster to Skiff	192.25.10.97--192.25.10.126

Joyce to Skiff	192.25.10.101--192.25.10.158

### Step 5: Convert to Binary
Let’s see the binary representation of important values to understand subnetting better.

Binary of 192.25.10.0

Decimal	Binary

192--11000000

25--00011001

10--00001010

0--00000000

Binary of 192.25.10.0:
11000000 00011001 00001010 00000000

Binary of Subnet Masks
/27 (255.255.255.224)

11111111 11111111 11111111 11100000
/30 (255.255.255.252)

11111111 11111111 11111111 11111100

### Final Notes
How do you determine subnet mask sizes?

Use the host formula: 2^h - 2 ≥ required hosts

Choose the smallest power of 2 that fits.

The number of network bits is 32 - h (gives CIDR notation).

How do you find broadcast addresses?

The last address in the subnet is always the broadcast address.

This is found by setting all host bits to 1 in binary.

How do you find the first and last usable host?

First usable IP = Network Address + 1

Last usable IP = Broadcast Address - 1

Summary Table

Subnet	Network	Subnet Mask	Usable IP Range	Broadcast

Foster	192.25.10.0	/27 (255.255.255.224)	192.25.10.1 - 192.25.10.30	192.25.10.31

Joyce	192.25.10.32	/27 (255.255.255.224)	192.25.10.33 - 192.25.10.62	192.25.10.63

Skiff	192.25.10.64	/27 (255.255.255.224)	192.25.10.65 - 192.25.10.94	192.25.10.95

Foster to Skiff	192.25.10.96	/30 (255.255.255.252)	192.25.10.97 - 192.25.10.98	192.25.10.127

Joyce to Skiff	192.25.10.100	/30 (255.255.255.252)	192.25.10.101 - 192.25.10.102	192.25.10.159

