# Tcpdump - Capture your first packet 

## Scenario 
You’re a network analyst who needs to use `tcpdump` to capture and analyze live network traffic from a Linux virtual machine.  

The lab starts with your user account, called `analyst`, already logged in to a Linux terminal.  

Your Linux user's home directory contains a sample packet capture file that you will use at the end of the lab to answer a few questions about the network traffic that it contains.  

Here’s how you’ll do this: **First**, you’ll identify network interfaces to capture network packet data. **Second**, you’ll use `tcpdump` to filter live network traffic. **Third**, you’ll capture network traffic using `tcpdump`. **Finally**, you’ll filter the captured packet data.  

## Solutions
1. Identify Network Interfaces.
   
* Use `ifconfig` to identify the interfaces that are available:

  `sudo ifconfig`  

<img width="718" height="335" alt="image" src="https://github.com/user-attachments/assets/b969df6a-1554-4d44-9982-020f7fb78b5e" />

* Use tcpdump to identify the interface options available for packet capture:

  `sudo tcpdump -D`
<img width="719" height="186" alt="image" src="https://github.com/user-attachments/assets/939b589b-8172-4897-ad3d-4e34aca22a5f" />

2. Inspect the network traffic of a network interface with tcpdump

* Filter live network packet data from the `eth0` interface with `tcpdump`:

  `sudo tcpdump -i eth0 -v -c5`

<img width="715" height="536" alt="image" src="https://github.com/user-attachments/assets/a6e41a34-8a71-45da-acb1-db3886af5341" />

This command will run tcpdump with the following options:

-`i eth0`: Capture data specifically from the eth0 interface.
-`v`: Display detailed packet data.
-`c5`: Capture 5 packets of data.

