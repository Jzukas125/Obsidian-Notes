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

Let's first look at the default configuration of the switch.

```
$ ovs-vsctl show
```

To add a VLAN and tags to a sub-interface, we need to modify the configuration through `ovs-vsctl`

```
$ ovs-vsctl set port <interface> tag=<0-99>
```

The tag should now be listed under the sub-interface in the configuration.

<h3> Tagging Unknown Traffic </h3>
The **Native VLAN** is used for any traffic that is not tagged and passes through a switch. To configure a native VLAN, we must determine what interface and tag to assign them, then set the interface as the default native VLAN. Below is an example of adding a native VLAN in Open vSwitch.

```
$ ovs-vsctl set port eth0 tag=10 vlan_mode=native-untagged
```

Now all traffic should be tagged, even with unknown origins.

<h3> Routing between VLANs </h3>
VLANs can connect to the internet using routers. Before modern solutions were introduced, network engineers would physically connect a switch and router separately for each VLAN present. 
Nowadays, that problem is solved through the **ROAS** (**R**outer **o**n **a S**tick) design. VLANs can now talk to routers using a switch port. 

The connection between the switch and router is known as a **trunk**.

VLANs are routed through the switch port, requiring only one trunk/connection between the switch and router, hence, "_on a stick_."

Before configuring the router, we must configure a trunk on a pre-existing connection. In our demonstration lab environment, trunks are configured by default as **bridges**. Each vendor configures their trunks and switch ports differently, some even with propriety protocols.

Below is an example of adding a new bridge and interface to create a trunk.

```
$ ovs-vsctl add-br br0
```

```
$ ovs-vsctl add-port br0 eth0 tag=10
```

Now, we can configure our router to route tagged traffic between VLANs. Remember, as mentioned when we introduced tags because the 802.1q tag is standardized, we only need to tell our router how to configure its switch port and what tags to accept for each interface.

Because all tagged traffic comes from a single connection, the router must be able to keep each tagged frame separate. This is accomplished using **virtual sub-interfaces**; these will act similar to physical interfaces and are commonly defined by the VLAN ID; the syntax for sub-interfaces is commonly, 
```
<name>.<vlan/sub-interface id> 
```

Below is an example of adding a new virtual sub-interface and configuring its corresponding addressing.

```
vyos@vyos-rtr# set interfaces ethernet eth0 vif 10 description 'VLAN 10'
```

```
vyos@vyos-rtr# set interfaces ethernet eth0 vif 10 address '192.168.100.1/24'
```

If all went well and was appropriately configured, we should be able to route traffic between VLANs while keeping traffic tagged and isolated!

But are they really isolated? Physically, they are isolated, but because routes exist between them, there is no security boundary, and they are not necessarily isolated. As long as a route exists between two VLANs, any device can communicate between the two.

# Common Secure Network Architecture

With the introduction of VLANs, there is a shift in network architecture design to include security as a key consideration. **Security**, **optimization**, and **redundancy** should all be considered when designing a network, ideally without compromising one component.

**Security zones** define **what** or **who** is in a VLAN and how traffic can travel **in** and **out**.  

Depending on whom you speak to, every network architect may have a different approach/opinion to the language or requirements surrounding security zones. In this task, we will immerse you in the most commonly accepted security zone standards, keeping a minimalist approach to segmentation.

|                          |                                                                                                                                                  |                                           |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------- |
| **Zone  <br>**           | **Explanation  <br>**                                                                                                                            | **Examples**                              |
| External                 | All devices and entities outside of our network or asset control.                                                                                | Devices connecting to a web server        |
| DMZ (demilitarized zone) | Separates untrusted networks or devices from internal resources.                                                                                 | BYOD, remote users/guests, public servers |
| Trusted                  | Internal networks or devices. A device may be placed in the trusted zone if there is no confidential or sensitive information.                   | Workstations, B2B                         |
| Restricted               | Any high-risk servers or databases.                                                                                                              | Domain controllers, client information    |
| Management               | Any devices or services dedicated to network or other device management. This zone is less commonly seen and can be grouped with the audit zone. | Virtualization management, backup servers |
| Audit                    | Any devices or services dedicated to security or monitoring. This zone is less commonly seen and can be grouped with management.                 | SIEM, telemetry                           |
While security zones mostly factor in what will happen internally, it is equally important to consider how new traffic or devices will enter the network, be assigned, and interact with internal systems. Most external traffic (HTTP, mail, etc.) will stay in the DMZ, but what if a remote user needs access to an internal resource? We can easily create rules for resources a user or device can access based on MAC, IP addresses, etc. We can then enforce these rules from network security controls; in the next task, we will discuss various access controls and solutions to implement policies.

Security zones and access controls will physically direct how and where traffic goes. But how is it decided what resources users or devices have access to? Traffic rules are often governed by company security policy or compliance as equally as security controls that determine access permissions.

We’ve now established a system to approach designing VLANs, but how can we practically implement and enforce them? In the next task, we will cover several protocols and applications that can be used to implement and enforce VLANs.

