# Lab 5-1

### Summary
We started the lab by making a network with 5 PCs, one router, and one switch, and later, we added a sniffer and replaced the switch with a hub for data collection. Using IPs like 192.168.X.X with subnets of 255.255.255.0 and Gateways relating to the IPs like 192.168.X.X to keep everything the same. PCs on the same switch must have the same default gateway. Then when we use the sniffer it can identify the packets going to and from HELLO! to PING ME! and we can see data switch up depending on if we're using a hub or switch.

### Commands 
There were no command prompts used in this lab other than maybe no shutdown if needed to be used in the CLI.

### Troubleshooting
Problem #1 started with getting the ping from HELLO! to PING ME! I started by turning on Simulation mode to see how far the packet had gone. It first wasn't moving past the PC itself which needed a simple gateway fix after experimenting. It then didn't go past the router which needed the port statuses to be turned back on which was randomly off which allowed the ping to get through.

Problem #2 was allowing the sniffer to work. You needed to connect a copper cross wire to the switch for it to connect for some reason.

### Other information
To connect to a router you must turn it off in the physical tab insert PT-ROUTER-NM-1CFE Modules into the router and turn it back on. You will then have places to connect PCs and/or Switches/sniffers etc. You then add IP addresses to the new ethernets and subnets. For example, I used the gateways for the other PCs as the IPs so it's easier to remember what to put.
