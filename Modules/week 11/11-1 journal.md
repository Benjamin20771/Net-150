# Lab 11-1 VLANs

### Summary
In this lab, we were given a file with three networks. We then had to connect them by using VLANs because the networks were all on separate floors. We then gave three VLANs to three sets of PCs (10,20,30). We then connected them through access and trunk ports. VLANs could then ping inside of themselves. 

### Commands
No specific commands were used in this lab, as everything was done in the config tab.

### Troubleshooting
No troubleshooting was needed, as the lab was pretty straightforward.

If troubleshooting was needed I could have maybe checked all switches for the VLANs or all PCs for IPs.

I could have also checked ports so they had the correct one selected.

### Entries 
#### Creating VLANs
To create a VLAN, you have to configure them on each switch. An example would be (10, ENG). Then, the Network address on the PC must match the number, so it is x.x.10.x. This makes the PC apart of the VLAN.

#### Access Ports 
Access ports are used mostly for Level 1/2 connections but not 2 2 connections. An example could be PC to switch, not switch to switch. These are the default ports but must have a specific VLAN number to connect with. 

#### Trunk Ports
Trunk ports are used for level 2 and above. Examples include switch to switch or switch to router. These must be changed from access to trunk, as they are not the default. Usually, they have all VLANs possible clicked but double-check to make sure it has them all, or if you don't want a specific one, then take it off.
