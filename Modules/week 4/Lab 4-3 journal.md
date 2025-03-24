# Lab 4-3

### Summary
In this lab, we use a packet tracer again to develop skills in a network to send messages through multiple switches and a router to get packets to the laptop/server. You must assign IPs and subnets and Default Gateways which we did last lab. We then used simulation mode which I filtered to HTTP packets which made it easier to spot the packet going from laptop to server. The laptop-to-server is seen by looking up the server's IP in the web browser on the laptop. Lastly, you can turn off and on the router in the physical tab by first saving NVRAM in the config tab and then turning it off and on which will save IPs.

### Commands
no shutdown- This command used in CLI is used to make sure router interfaces are ON or as it says in CLI UP.

### Troubleshooting
The router would not connect to either switch until I used the no shutdown command but I had to use it twice so it could turn ON or UP both of them which allowed the successful ping.

### Extra Information 
The Simulation mode = Clear all activity to make room, edit the filter to HTTP, and send the packet, the loss of HTTP-only packets comes through as we see it go from device to device.

Saving configurations = You can turn off and on the router in the physical tab by first saving NVRAM in the config tab and then turning it off and on which will save IPs. Use the speed-up button to get the IPs back faster.

Packet tracer tips- Use the CLI tab to see what ethernets are connected to what devices if you forget. 
        ----- You can reset the simulation after you find what specific packet you want and filter it so it's easier to see.
