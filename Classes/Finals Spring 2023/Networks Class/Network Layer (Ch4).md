#College 
Datacenter network - 10s to 100's of thousands of hosts, often closely coupled in proximity: e-business, content-servers, search engines

Network Layer - transport segment from sending to receiving host 
- Sender - encapsulates segments into data grams, passes to link layer
- Receiver - delivers segments to transport layer to protocol 
-Routers - examine header fields in IP data grams passing through and moves data grams from input ports to output ports to transfer data grams along end-to-end path

Network Layer - data plane, control plane 
- Data Plane: local, per-router function, determine how data grams arrive at router input ports and how they're forwarded to router output ports.
- Control plane: network-wide logic, determines how data grams are routed among routers along end-to-end paths from source host to destination host

Per-router control plane - Individual routing algorithm components in each and every router interact in the control plane.


![[Pasted image 20230926125410.png]]

Input port functions - decentralized switching -- use header field values and lookup ports using forwarding tables in input port memory 

Input port functions passes through the physical layer, the link layer and then decentralized switching.

Subnets are device interfaces that can physically reach each other. IP addresses have structure which include subnet parts and host parts. Subnet parts are devices in the same subnet that have common high order bits. Host parts are just remaining low order bits.

Subnets are defined by detaching each interface from its host or router, creating "islands" of isolated networks, each isolated network is called a subnet.

IP addressing: CIDR: Classless InterDomain Routing (cider) - this is the subnet portion of an address of arbitrary length
![[Pasted image 20230926130737.png]]

