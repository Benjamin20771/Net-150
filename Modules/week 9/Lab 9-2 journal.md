# Lab 9-2

### Summary
We made two networks with two routers/4switches/5Pcs. 

This lab was to practice static routing and help with basic networking. Getting the chart together wasn't difficult, but there were some things to remember, like jumping numbers for specific things.

<img width="933" alt="image" src="https://github.com/user-attachments/assets/b75837a4-72f2-4086-9a58-f62c9722db10" />

<img width="593" alt="image" src="https://github.com/user-attachments/assets/4213997a-a9a4-4fbc-888f-4ac874c93dd8" />


### Commands 

#### West Router 

Router(config)#ip route 154.103.19.0 255.255.255.128 192.168.0.2

Router(config)#ip route 154.103.19.128 255.255.255.192 192.168.0.2

#### East Router

Router(config)#ip route 154.103.16.0 255.255.254.0 192.168.0.1

Router(config)#ip route 154.103.18.0 255.255.255.0 192.168.0.1

### Troubleshooting

The only problem I ran into was static routing the Finance East as I needed a 128 rather than a 0 for the IP route because they were both x.x.19.x. Remember to jump


