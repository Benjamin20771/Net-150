# Lab 10-1

### Summary
In this lab, we were given a file to download and it was three networks where we wanted to set up the RIP (v2) on the routers. With this, we put commands into CLI(see below) and connected the routers. We then turned on simulation mode to see RIPv2 packets from different routers to see what it was doing. 

### Commands 

enable-allows commands into CLI

config terminal- allows the access to edit the terminal

router rip- allows access to the RIP section of the terminal

version 2- Makes rip version 2

network x.x.x.x-This adds a network address to the rip of the router

show ip route- This shows information based on the connections with the router.

Note-RIP doesn't need a subnet cuz it automatically steals it from the router itself

### Troubleshooting

I had problems putting commands into the CLI so I had to look into my past journals and see that I was forgetting the "enable" command 

### Extra Notes
When inputting the networks into the router make sure to obtain all networks that are connected to the router so they know that they can communicate with each other. I like to think of it as a friend group. Bob is router 1. He knows himself and Alex who is router 2. He wants to deliver a message to jean who is router 3 but doesn't know him well enough. Bob who knows Ales says to deliver a message to jean. Alex knows Bob herself and jean so she send the message to jean. Jean only knows Alex and himself but since it came from alex he understands the message 
