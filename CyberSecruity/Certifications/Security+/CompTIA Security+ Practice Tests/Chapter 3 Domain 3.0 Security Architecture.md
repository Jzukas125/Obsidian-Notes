#Securityplus
# 1-10
1. A
2. A
3. ~~A~~
4. C
5. C
6. B
7. B
8. C
9. ~~A~~
10. ~~D~~
7/10

3 B is correct
Enrique is concerned about backup data being infected by malware. The company backs up key servers to digital storage on a backup server. Which of the following would be most effective in preventing the backup data being infected by malware?
A. Place the backup server on a separate VLAN.
B. Air gap the backup server.
C. Place the backup server on a different network segment.
D. Use a honeynet.

Air gapping refers to the server not being on a network. This means literally that there is "air" between the server and the network. This prevents malware from infecting the backup server. A separate virtual local area network or physical network segment can enhance security but is not as effective as air gapping.

9 D is correct
Which of the following is not an advantage of a serverless architecture?
A. It does not require a system administrator.
B. It can scale as function call frequency increases.
C. It can scale as function call frequency decreases.
D. It is ideal for complex applications.

Serverless architectures do not require a system admin because the provider manages the underlying function as a service (FaaS).

10 B is correct
Which of the following is the most important benefit from implementing SDN?
A. It will stop malware.
B. It provides scalability.
C. It will detect intrusions.
D. It will prevent session hijacking.

SDN (software defined networking) makes the network very scalable, making it very easy to add or remove resources.

# 11-20
11. ~~D~~
12. ~~A~~
13. ~~B~~
14. D
15. ~~C~~
16. B
17. A
18. C
19. ~~A~~
20. ~~A~~
4/10

11 A is correct
Derek has been asked to implement his organization’s service-oriented architecture as a set of microservices. What does he need to implement?
A. A set of loosely coupled services with specific purposes
B. A set of services that run on very small systems
C. A set of tightly coupled services with custom-designed protocols to ensure continuous
operation
D. A set of services using third-party applications in a connected network enabled with
industry standard protocols

A microservice architecture builds applications as a set of loosely coupled services that provide specific functions using lightweight protocols. It does not define the size of the systems, but it is not a tightly coupled environment. Protocol choice is often open standards-based, but the emphasis is on lightweight protocols. There is not a requirement that services be in-house or third party exclusively. 

12 C is correct
Abigail is responsible for datacenters in a large, multinational company. She has to support multiple datacenters in diverse geographic regions. What would be the most effective way for her to manage these centers consistently across the enterprise?
A. Hire datacenter managers for each center.
B. Implement enterprise-wide SDN.
C. Implement infrastructure as code (IaC).
D. Automate provisioning and deprovisioning.

The correct answer is to implement IaC. Infrastructure as code is the process of managing and provisioning computer datacenters through machine-readable definition files, rather than physical hardware configuration or interactive configuration tools. Datacenter managers won't necessarily provide consistent management.

13 C is correct
Naomi wants to secure a real-time operating system (RTOS). Which of the following
techniques is best suited to providing RTOS security?
A. Disable the web browser.
B. Install a host firewall.
C. Use secure firmware.
D. Install antimalware software.

Using secure firmware, as well as using an RTOs with time and space partitioning, are both common methods to help ensure RTOs security. Unlike traditional operating systems, real-time operating systems are used in applications where they need to deal with inputs immediately. 

15 D is correct
Madhuri has configured a backup that will back up all of the changes to a system since the last time that a full backup occurred. What type of backup has she set up?
A. A snapshot
B. A full backup
C. An incremental backup
D. A differential

Differential backups back up all of the changes since the last full backup. An incremental backup backs up all changes since the last incremental backup. An incremental backup only copies modified data since the last backup.

19 D is correct
Mia is a network administrator for a bank. She is responsible for secure communications
with her company’s customer website. Which of the following would be the best for her to
implement?
A. SSL
B. PPTP
C. IPSec
D. TLS

Transport Layer Security (TLS) provides a reliable method of encrypting web traffic. TLS is the successor to SSL.

20 B is correct
Nora has rented a building with access to bandwidth and power in case her organization ever experiences a disaster. What type of site has she established?
A. A hot site
B. A cold site
C. A warm site
D. A MOU site

A cold site is a location that can be brought online but does not have systems, cold sites typically have access to power and bandwidth, but they need to be fully equipped to operate after a disaster since they are just rented space.

# 21-30
21. C
22. A
23. ~~D~~
24. D
25. B
26. ~~A~~
27. ~~A~~
28. ~~A~~
29. ~~C~~
30. D
5/10

23 A is correct
Elaine wants to adopt appropriate response and recovery controls for natural disasters.
What type of control should she use to prepare for a multi-hour power outage caused by a
tornado?
A. A hot site
B. A generator
C. A PDU
D. A UPS

A generator is the most appropriate answer to a multi-home outage. Although a hot site would allow her to do as she wished, it would cost significantly more. UPS systems are not typically designed to handle long outages. 

26 B is correct
Chris is preparing to implement an 802.1X-enabled wireless infrastructure. He knows that
he wants to use an Extensible Authentication Protocol (EAP)-based protocol that does not
require client-side certificates. Which of the following options should he choose?
A. EAP-MD5
B. PEAP
C. LEAP
D. EAP-TLS

PEAP, the protected extensible authentication protocol relies on server-side certificates and on tunneling to ensure communications security. EAP-MD5 is not recommended for wireless networks and  does not support mutual authentication. LEAP, the Lightweight Extensible Authentication Protocol, uses WEP keys for its encryption and is not recommended due to security issues. Finally, EAP-TLS, or EAP Transport Layer Security, requires certificates on both the client and server, consuming more management overhead.

27 C is correct
Olivia is implementing a load-balanced web application cluster. Her organization already
has a redundant pair of load balancers, but each unit is not rated to handle the maximum
designed throughput of the cluster by itself. Olivia has recommended that the load balancers
be implemented in an active/active design. What concern should she raise as part of this
recommendation?
A. The load balancer cluster cannot be patched without a service outage.
B. The load balancer cluster is vulnerable to a denial-of-service attack.
C. If one of the load balancers fails, it could lead to service degradation.
D. The load balancer cannot handle the throughput due to having two active nodes.

Olivia should make her organization aware that a failure in one of the active nodes would result in less maximum throughput and a potential for service degradation. Since services are rarely run at maximum capacity, and many can have maintenance windows scheduled, this does not mean that the load balancers cannot be patched.

28 C is correct
Mark is responsible for managing his company’s load balancer and wants to use a loadbalancing scheduling technique that will take into account the current server load and active
sessions. Which of the following techniques should he choose?
A. Round-robin
B. Weighted response time
C. Least connection
D. Source IP hashing

29 D is correct
Ramon is building a new web service and is considering which parts of the service should use
Transport Layer Security (TLS). Components of the application include:
1. Authentication
2. A payment form
3. User data, including address and shopping cart
4. A user comments and reviews section
Where should he implement TLS?
A. At points 1 and 2, and 4
B. At points 2 and 3, and 4
C. At points 1, 2, and 3
D. At all points in the infrastructure

All cases are correct due to TLS's overhead being minimal

# 31-40
31. ~~A~~
32. C
33. ~~D~~
34. A
35. ~~A~~
36. ~~B~~
37. ~~A~~
38. ~~C~~
39. ~~C~~
40. ~~B~~
2/10

31 D is correct
Charles wants to use IPSec and needs to be able to determine the IPSec policy for traffic
based on the port it is being sent to on the remote system. Which IPSec mode should he use?
A. IPSec tunnel mode
B. IPSec PSK mode
C. IPSec IKE mode
D. IPSec transport mode

IPsec transport mode allows different policies per port. IPSec doesn't have a PSK mode, but WPA2 does. IKE is used to set up security associations in IPSec but doesn't allow this type of mode setting.

33 D is correct
Jason wants to implement a remote access virtual private network (VPN) for users in his
organization who primarily rely on hosted web applications. What common VPN type is best
suited to this if he wants to avoid deploying client software to his end-user systems?
A. A TLS VPN
B. An RDP (Remote Desktop Protocol) VPN
C. An Internet Control Message Protocol (ICMP) VPN
D. An IPSec VPN

A TLS VPN is frequently chosen when ease of use is important, and web applications are the primary usage mode. RDP is a remote access tool, not a VPN tool, and ICMP is used for things like ping, not for VPN. IPSec VPNs are used for site-to-site VPNs and for purposes where other protocols may be needed, because they make the end-point system 

35 D is correct
What IP address does a load balancer provide for external connections to connect to web
servers in a load-balanced group?
A. The IP address for each server, in a prioritized order
B. The load balancer’s IP address
C. The IP address for each server in a round-robin order
D. A virtual IP address

Load balancers provide a virtual IP, or VIP. Traffic sent to the VIP is directed to servers in the pool based on the load-balancing scheme that that pool is using - often a round-robin scheme, but other versions that include priority order and capacity tracking or ratings are also common

36 A is correct
Port security filters by mac address.

37 C is correct
Authentication headers provide complete packet integrity, authenticating the packet and the header.

38 A is correct
Network taps copy all traffic to another destination, allowing traffic visibility without a device inline.

39 B is correct
Internet Key exchange IKE, is used to set up security associations on each end of the tunnel. 

40 A is correct
Port mirroring allows the traffic segment to be copied to the segment were the nips is installed.

# 41-50
41. D
42. ~~A~~
43. ~~D~~
44. A
45. ~~C~~
46. C
47. A
48. C
49. A
50. D
7/10

42 B is correct
Ryan is concerned about the security of his company’s web application. Since the application
processes confidential data, he is most concerned about data exposure. Which of the following would be the most important for him to implement?
A. WAF
B. TLS
C. NIPS
D. NIDS

The correct answer is to encrypt everything using TLS. A WAF is a good idea but it is not the most important thing to implement.

43 C is correct
Claire has been notified of a zero-day flaw in a web application. She has the exploit code,
including a SQL injection attack that is being actively exploited. How can she quickly react
to prevent this issue from impacting her environment if she needs the application to continue
to function?
A. Deploy a detection rule to her IDS.
B. Manually update the application code after reverse-engineering it.
C. Deploy a fix via her WAF.
D. Install the vendor-provided patch.

Claire's best option is to fix it via WAF that will detect SQL injections. Vendor patches for zero days typically take some time to come out.

45 D is correct
Next-generation firewalls include many cutting-edge features. Which of the following is not a common next-generation firewall capability?
A. Geolocation
B. IPS and/or IDS
C. Sandboxing
D. SQL injection

Although NGFWs provide may defensive capabilities, SQL injection is an attack instead of a defense. 

# 51-60
51. ~~A~~
52. ~~B~~
53. A
54. D
55. D
56. A
57. ~~B~~
58. A
59. B
60. ~~C~~
6/10

51 D is correct
Jason is considering deploying a network intrusion prevention system (IPS) and wants to be
able to detect advanced persistent threats (APTs). What type of IPS detection method is most
likely to detect the behaviors of an APT after it has gathered baseline information about
normal operations?
A. Signature-based IPS detections
B. Heuristic-based IPS detections
C. Malicious tool hash IPS detections
D. Anomaly-based IPS detections

Anomaly-based detection systems build a behavioral baseline for networks and then assess differences from those baselines. Signature and hash based look for known threats.

52 A is correct
Mila wants to generate a unique digital fingerprint for a file, and needs to choose between a
checksum and a hash. Which option should she choose and why should she choose it?
A. A hash, because it is unique to the file
B. A checksum, because it verifies the contents of the file
C. A hash, because it can be reversed to validate the file
D. A checksum, because it is less prone to collisions than a hash

Mila should select a hash because is designed to be unique to each input. That means that multiple files could have the same checksum value.

57 C is correct
Mateo wants to conduct a fail over test for his datacenter. What will he need to do to accomplish this?
A. Turn off all systems in his datacenter.
B. Simulate what would occur during a datacenter outage.
C. Force a fail over using his network or other systems.
D. Cause an outage of a critical system.

Datacenters have a fail over process that can be manually executed in case of emergency. Mateo should use that process to fail over to his organization's fail over site. Simulation is not a fail over test, and creating an outage of a critical system typically will not cause an entire datacenter to fail over.

60 B is correct
Brandon deploys a server in a VLAN used for IoT devices. He then creates firewall rules that
allow users in a system administration network to SSH to that server so that they can manage systems in the protected network segment. What type of solution has Brandon deployed?
A. A UTM
B. A jump server
C. An ICS server
D. A VPN

Jump servers are used to access secured zones and are typically carefully controlled and monitored because they are the single point of entry from untrusted environments.

# 61 - 70
61. ~~D~~
62. B
63. ~~C~~
64. ~~C~~
65. B
66. D
67. B
68. ~~A~~
69. C
70. B
6/10

61 C is correct
What protocol is commonly used to allow for secured tunnels between corporate networks
through untrusted networks?
A. RTOS
B. SHA-1
C. IPSec
D. RSA

IPSec virtual private networks are commonly established to tunnel through public or untrusted networks. RTOs or real time operating system, is used embedded systems. 