# Lab 6-2

### Summary of Classful Subnetting
This lab was interesting for me because I struggled with it a decent amount. We made three separate networks and connected them all. The photo below helped out a lot as it explained what to use the IPs for. 

### Commands

Not many commands unless you want to use the GUI area to fill in information.

Tip-You can see how to do commands when you fill out the information manually on the bottom

### Troubleshooting

Even though this lab was difficult there wasn't much troubleshooting but there are some tips I used.

1. Check that everything has the 255.255.255.224 CIDR-/27.

2. Check that the PCs are using the first and last usable IPs.

3. Check that the router IP is equal to the gateways of the PCs

4. Make sure every router has a RIP involved

5. Make sure that serial numbers are one after the other from 1 router to another

6. The first PDU send will fail. try again

7. Make sure switches and routers are connecting both GigabitEthernets

8. Ensure that everything within the network can ping each other

9. Use the Simulation mode to see where the PDU is stopping. This can help with seeing where the problem is.

### Other Information

The router IP has to be the default gateway of the PCs connected to that router. 

You must have an RIP involved when connecting routers to tell each other what network to look for.

![283FD300-6C59-46E6-AE82-622041CD0AD6_1_201_a](https://github.com/user-attachments/assets/0beac329-09b5-459c-84f1-d4cedaf99eb3)
