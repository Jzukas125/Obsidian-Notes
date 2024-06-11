A properly designed network permits not only internet usage and device communication but also redundancy, optimization, and security. In a well designed network, if a switch goes down, then packets can be redistributed through another route with no loss in uptime. If a web server is compromised, it cannot traverse the network and access important information. A system administrator should be confident that their servers are secure if a random device joins a network and cannot access those systems. 

All of these concepts and scenarios are what separate a functional network from a well-designed network.

Throughout this room, we will break down these scenarios or objectives and understand different concepts we can use to implement them in a network. We will also discuss potential threats a network may face even after proper best practices are established.

<h3> Learning Objectives </h3>
1. Understand the principles of secure network architecture design
2. Learn and implement common network security concepts and protocols
3. Understand a network’s environment and potential threats

# Network Segmentation

<h3> The need for secure segmentation </h3>
Subnets seem to solve all problems a network may face; why would we use another solution? To answer this question, let’s consider a scenario where a client brings in their own device, a common practice known as BYOD (Bring Your Own Device). The client’s device was infected with a Remote Access Trojan (RAT) that will attempt to traverse the network the device is connected to and exfiltrate any sensitive information. With subnetting in place, there is no restriction in place as to where the infected device could connect as long as the proper routes are in place, leaving sensitive information and servers open to the unknown device. How do we fix this problem? VLANs! 

VLANs are used to segment portions of a network at layer two and differentiate devices. 

VLANs are configured on a switch by adding a "tag" to a frame. The 802.1q or dot1q tag will designate the VLAN that the traffic originated from.