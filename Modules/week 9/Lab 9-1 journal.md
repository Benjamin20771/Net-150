# Lab 9-1 Static Routing

### Summary
In this lab, we were given a network where everything is set up (good use of reference if ever needed) and we have to set up the static IP routes for each router. Below everything is explained/shown.

### Screenshots
Router 3:

<img width="249" alt="image" src="https://github.com/user-attachments/assets/5ecc0268-1ed4-414a-8b17-fbe7c58df3d1" />

Router 2:

<img width="169" alt="image" src="https://github.com/user-attachments/assets/bc0a7b24-d4dc-46f4-908e-21502a25cdbb" />

Router 1:

<img width="171" alt="image" src="https://github.com/user-attachments/assets/2d1fd835-4e73-48ce-a4c0-0d91288e02f8" />

### Commands

"show ip route" = This shows information based on the connections with the router.

"config terminal" = This allows us to set up the static routes

### show ip route info

#### “Show IP route” for R1
 
10.0.0.0/24 is subnetted, 2 subnets
	–This means R1 is connected to 2 different subnets or networks R2 and R3

C 10.10.10.0 is directly connected, Serial0/0/1
	–This is the connection to the R3 network

C 10.10.20.0 is directly connected, Serial0/0/0
	–This is the connection to the R2 network

S 192.168.10.0/24 [1/0] via 10.10.10.2
	–This is the acknowledgment that network 1 connection to the R3 

C 192.168.20.0/24 is directly connected, FastEthernet0/1
	–This is the connection of Network 2 to the R1

S 192.168.30.0/24 [1/0] via 10.10.20.2
	–This is the acknowledgment that network 3 connected to the R2 
 
#### “Show IP route” for R3

10.0.0.0/24 is subnetted, 1 subnet
	–This means that R3 is connected to R1 as it doesn’t need to be connected directly to R2
 
C 10.10.10.0 is directly connected, Serial0/0/0
	–This is its connection to R1

C 192.168.10.0/24 is directly connected, FastEthernet0/0
	–This is the Network 1 connection to R3

S 192.168.20.0/24 [1/0] via 10.10.10.1
	–This is the acknowledgment that network 2 is connected to R1

S 192.168.30.0/24 [1/0] via 10.10.10.1
	–This is the acknowledgment that network 3 is connected to R2



### Conclusion
In conclusion in this lab, we get very useful information on static routing and how it works when making a network. I will refer to this lab as needed as it is extremely helpful
