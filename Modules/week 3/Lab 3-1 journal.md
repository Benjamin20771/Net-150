# Lab 3-1

### Summary
In this lab I, and for some parts a partner, have discovered how to look at how MAC and IP addresses intercoprate by using wireshark to analyze the ARP traffic while we ping IP addresses on the Command prompt. This lab was looking at differnt information in ARP traffic.

### Useful Commands 
-arp -d = This clears all ARP traffic on the wireshark application 

-ping = This is used usually with IP addresses to look at traffic or to test internet connection with another device

-netsh interface ip delete arpcache = This is the same as the arp -d but only on linux

### Problems/Troubleshooting
The only problem I had ran into was not being able to ping my neighbor or visversa so I had remembered from cybersecurity that the firewall must be down for anythying to get through

### Other information
Other information on the wireshark capture could be specific frame or bytes on that wire
