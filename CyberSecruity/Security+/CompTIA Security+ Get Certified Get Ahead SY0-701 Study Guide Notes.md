#Securityplus
These notes follow the CompTIA Security+ Get Certified Get Ahead SY0-701 text book which can be bought at [any online book retailer](https://www.thriftbooks.com/w/comptia-security-get-certified-get-ahead-sy0-701-study-guide_darril-gibson_joe-shelley/51506429/#edition=70312038&idiq=62261995)

This is by no means a copy of the original textbook and all of the copy right goes towards the original book (CompTIA Security+ Get Certified Get Ahead SY0-701 Study Guide) and the authors, Darril Gibson and Joe Shelley. These notes are in no means attempting to recreate or copy the works of the author or the textbooks. This was used in tandem with the textbook by me to help organize and understand its  contents.
# Chapter 1

Redundancy adds duplication to critical systems and provides fault tolerance. If a critical component has a fault, the redundancy's duplication allows the service to continue without interruption.

Scalability is increasing the capacity of a service
	Horizontal scaling is adding more machine or nodes to a system
	Vertical Scaling involves adding more power such as CPU, RAM, storage, etc
	Elasticity automates scalability 

Security Controls
	Technical Controls use tech as hardware, software, and firmware
	Managerial Controls are primarily admin controls
	Operational Controls help ensure the day-to-day operations of an organization comply with the security policy
	Physical controls impact the physical world

Control categories - describe how the control works
	Technical controls 
		Encryption
		Antivirus software
		Intrusion detection systems and Intrusion prevention systems
		Firewalls
		Least privilege
	Managerial Controls
		Risk assessments
		Vulnerability assessments
	Operational Controls
		Awareness and Training
		Configuration management
		Media protection
	Physical Controls
		physical controls are any controls that you can physically touch

Chapter 1 review

CIA triad 
Basic Risk Concepts 
Security Controls
Understanding logs

Chapter 1 Practice Questions
1. C 
2. B
3. A
4. ~~B~~
5. D
6. C
7. D
8. A
9. B
10. ~~A~~
11. C
12. ~~C~~
13. B
14. ~~D~~
15. D

Chapter 1 questions review
4 A is correct, Elasticity is the best choice because it allows the server to dynamically scale as needed in response to changes in demand. Scalability isn't the best answer because it is done manually; in this case, the high resource usage is random and manually adding resources can't respond to the random spikes quickly enough. Normalization refers to organization tables and columns in a database to reduce redundant data and improve overall database performance. Stored procedures are a group of SQL statements that execute as a whole and help prevent SQL injection attacks.

10 D is correct. 
Kate’s manager asked her to organize a new process for conducting periodic vulnerability assessments of her organization’s infrastructure. She is working to create a standard operating procedure for this scanning. What category BEST describes the control is she creating? 
A. Technical B. Detective C. Physical D. Managerial
Tricky question because there are several possible correct answers but not the BEST answer. Vulnerability assessments are an assessment method used to reduce risk and are an assessment method used to reduce risk and are an example of managerial control. The clues that is managerial is the correct answer here are that there is no mention of the technology being used are that there is no mention of the technology being used to complete the assessments and there is no focus on policy and procedure.

12 D is correct
You are investigating an active security incident and you
want to view the contents of network traffic that passed
between two systems. What data source would BEST
provide this information?
A. Operating system log
B. Application log
C. Firewall log
D. Packet capture
Investigators looking into an active security incident may use a packet capture tool like Wireshark to capture network traffic. Firewall logs may contain records of the systems that communicated with each other, but they would not normally contain the content of the communication. Operating system and application logs are not an ideal source of this type of info because they only pertain to one computer or application and would not have access to all content of network traffic

14 A is correct
The network time protocol (NTP) is used to synchronize system clocks with a centralized time source. The file transfer protocol (FTP) and secure file transfer protocol (SFTP) are used to transfer files and not synchronize clocks. The hyper text transfer protocol secure (HTTPS) is used to transfer web pages and not to synchronize clocks.

11/15 correct 


# Chapter 2 

AAA - Authentication, authorization, and accounting work together with identification to provide a comprehensive access management system.

Authentication - the process or action of proving or showing something to be true
Authorization - the tight or permission that is granted to a system entity to access a system resource 
Accounting - measures the resources the user consumes during access

Something you know is like a pin or password

Something you have refers to something you can physically hold such as a smart card, security key, software token, and hardware token
Soft token is like a google authenticator app
Hard token is an electronic device that has a one time password displayed on it

Something you are is biometrics such as fingerprints, vein matching, retina imaging, iris scanners, facial recognition, voice recognition, and gait analysis (walking analysis)

Chapter 2 Questions
1. D,F
2. ~~B~~
3. ~~C~~
4. ~~B~~
5. B
6. ~~C~~
7. C
8. ~~D~~
9. ~~B~~
10. D
11. ~~A~~
12. ~~A~~
13. D
14. B
15. C

Chapter 2 Questions review

2 A is correct
Your organization recently updated an online application
employees use to log on when working from home.
Employees enter their username and password into the
application from their smartphone and the application logs
their location using GPS. Which type of authentication is
being used?
A. One-factor
B. Dual-factor
C. Something you are
D. Something you have

It is asking what type of authentication is being used and it is one-factor as it is only one factor of authentication

3 B is correct
Management within your organization wants to add 2FA
security for users working from home. Additionally,
management wants to ensure that 2FA passwords expire
after 30 seconds. Which of the following choices BEST
meets this requirement?
A. HOTP
B. TOTP
C. SMS
D. Kerberos

A time based one time password (TOTP) meets the requirement of two-factor authentication (2FA) A user logs on with regular credentials and then must enter an additional one-time password. An example of this is google authenticator.
A HMAC-based One-Time Password (HOTP) creates passwords that do no expire until they are used. Short message service (SMS) is sometimes used to send users a one-time use password via email. Kerberos uses tickets instead of passwords

4 C is Correct 
 Management within your organization has decided to
implement a biometric solution for authentication into the
data center. They have stated that the biometric system
needs to be highly accurate. Which of the following provides
the BEST indication of accuracy with a biometric system?
A. The lowest possible FRR
B. The highest possible FAR
C. The lowest possible CER
D. The highest possible CER

A lower crossover error rate (CER) indicates a more accurate biometric system. False acceptance rate (FAR) and the False rejection rate (FRR) vary based on the sensitivity of the biometric system and don't indicate accuracy by themselves. A higher CER indicates a less accurate biometric system.

6 D is correct
Users regularly log on with a username and password.
However, management wants to add a second
authentication factor for any users who launch the gcga
application. The method needs to be user-friendly and nondisruptive. Which of the following will BEST meet these
requirements?
A. An authentication application
B. TPM
C. HSM
D. Push notifications

Push notifications are user friendly and non disruptive. An authentication application isn't as user-friendly as a push notification. It requires users to log on to the smartphone, find the app, and enter the code. A trusted platform module (TPM) can provide for the implementation of full disk encryption, which would protect the data if someone accessed the laptop, but it doesn't prevent access. A hardware security module (HSM) isn't relevant to the question as well as TPM.

8 A is correct
You need to provide a junior administrator with appropriate
credentials to rebuild a domain controller after it suffers a
catastrophic failure. Of the following choices, what type of
account would BEST meet this need?
A. User account
B. Generic account
C. Guest account
D. Service account
A user account with admin privileges can have the admin add the domain controller. A generic account is shared between two or more users and is not recommended. A guest account is disabled by default and it is not appropriate to grant the guest account admin privileges. A service account is an account created to be used by a service  

9 D is correct 
 Lisa is reviewing an organization’s account management
processes. She wants to ensure that security log entries
accurately report the identity of personnel taking specific
actions. Which of the following steps would BEST meet this
requirement?
A. Implement generic accounts.
B. Implement role-based privileges.
C. Use an SSO solution.
D. Remove all shared accounts.
Removing all shared accounts is the best answer of the available choices. If two employees are using the same account, and one employee maliciously deletes data in a database, it isn't possible to identify which employee deleted the data. Generic accounts are the same as shared accounts and shouldn't be used. Role-based privileges assign the same permissions to all members of a group, which simplifies administration. A single sign-on (SSO) solution allows a user to log on once and access multiple resources.

11 C is correct
A software developer is creating an application that must
access files stored in the user’s Google Drive. What is the
best way for the user to grant the application access to their
Google account?
A. OpenID Connect
B. Provide their Google password each time they log
into the application
C. OAuth
D. Store their Google password in the application
The OAuth authorization protocol is explicitly designed for this type of situation. Use of the application can grant the application limited access to resources in their Google account without disclosing their credentials. OpenID connect is used to log into one service with credentials with another service and does not provide the type of authorization required in this scenario.

12 B is correct 
Web developers in your organization are creating a web
application that will interact with other applications running
on the Internet. They want their application to receive user
credentials from an app running on a trusted partner’s web
domain. Which of the following is the BEST choice to meet
this need?
A. SSO
B. SAML
C. Kerberos
D. RADIUS
Security Assertion Markup Language (SAML) is a single sign-on (SSO) solution used for web-based applications and would meet the requirement. All SSO are not used on the internet. Kerberos is an SSO solution used on internal networks such as in Microsoft Active Directory domains and Unix realms. Remote Authentication Dial-In User Service (RADIUS) provides AAA services for some remote access, wired, and wireless network solutions.
7/15 correct
# Chapter 3 

OSI model, UDP, IP, TCP
ICMP - Internet Control Message Protocol tests basic connectivity and includes tools like ping and tracert

Address Resolution Protocol (ARP) - Resolves IPv4 addresses to MAC addresses 

Bridge protocol data unit - messages sent by STP in a network to detect loops

Security zones
	Intranet - internal network, people use the intranet to communicate and share content with each other 
	Extranet - part of a network that can be accessed authorized entities outside of the network

Screened Subnet ie DMZ - a security zone between a private network and the internet

Network address translation (NAT) - protocol that translates public IP addresses to private IP and private IP addresses back to public 

VLANS can use switches to separate networks 

Control plane vs Data plane
	control plane - communications used to control and configure the network take place here
		Core components include the Policy Engine, Policy Administrator, and the Policy Enforcement Point
	data plane - software used to communicate with each other take place here

Ports to know
	22 - ssh
	80 - HTTP
	443 - HTTPS
	587 - SMTPS

Chapter 3 Questions 
1. ~~A~~
2. B
3. C - Guess
4. D
5. A
6. ~~C~~
7. B
8. A
9. ~~D~~
10. A
11. ~~D~~
12. ~~C~~
13. ~~B~~
14. ~~C~~
15. ~~A, E~~

Chapter 3 Questions Review 

1 B is correct
An outside consultant performed an audit of the Municipal
House of Pancakes network. She identified a legacy protocol
being used to access browser-based interfaces on switches
and routers within the network. She recommended
replacing the legacy protocol with a secure protocol to
access these network devices using the same interface.
Which of the following protocols should be implemented?
A. The newest fully supported version of SSL
B. The newest fully supported version of TLS
C. The newest fully supported version of LDAPS
D. The newest fully supported version of SNMP
The newest version of Transport Layer Security (TLS) should implemented to access the network devices to access the network devices. SSL has been deprecated and should not be used. Lightweight Directory Access Protocol Secure is used to communicate with directories such as Microsoft Active Directory. Simple Network Management Protocol version 3 (SNMPv3) adds security to SNMP and encrypts the credentials sent to and from the network devices, but it doesn't support access via a browser 

3 C is correct 
Maggie needs to collect network device configuration
information and network statistics from devices on the
network. She wants to protect the confidentiality of
credentials used to connect to these devices. Which of the
following protocols would BEST meet this need?
A. SSH
B. FTPS
C. SNMPv3
D. TLS
Simple Network Management Protocol version 3 is a secure protocol that can monitor and collect information from network devices. It includes strong authentication mechanisms to protect the confidentiality of credentials.

6 B is correct
Maggie is examining traffic on a network searching for signs
of insecure protocol use. She sees communications taking
place on several different network ports. Which one of these
ports most likely contains insecure traffic?
A. 22
B. 80
C. 443
D. 587
 Port 80 is used by the unencrypted HTTP. Secure web communications should take place using the encrypted HTTPS on port 443. Port 22 is used by SSH for encrypted administrative connections and data transfers. Port 587 is used by the Simple Mail Transfer Protocol Secure (SMTPS) to transfer email messages between servers over an encrypted connection.

9 B is correct
 Network administrators manage network devices remotely.
However, a recent security audit discovered they are using a
protocol that allows them to send credentials over the
network in cleartext. Which of the following is the best
method to be adopted to eliminate this vulnerability?
A. Use SNMPv2c.
B. Use SSH.
C. Use SSL.
D. Use SFTP.
Secure Shell can be used to connect ot many network devices and is the best answer of the given choices. SSL encrypts but has been deprecated and shouldn't be used. SFTP just transfers files.

11 B is correct
Your organization’s network looks like the following graphic,
and you’ve been asked to verify that Firewall 1 has the
correct settings.
All firewalls should enforce the following requirements:
Use only secure protocols for remote management.
Block cleartext web traffic.
The following table shows the current rules configured in Firewall
1.
You’re asked to verify the rules are configured correctly. Which
rule, if any, should be changed to ensure Firewall 1 meets the
stated requirements?
A. HTTPS Outbound
B. HTTP Outbound
C. DNS
D. Telnet
E. SSH
F. None. All rules are correct.
(Figure not shown)
HTTP rule should be changed from Allow to Block to block cleartext web traffic. Telnet rule has the incorrect destination address and the incorrect action. It should be 10.0.1.0/24 and set to block because it is not a secure protocol for remote management

12 A is correct
The Springfield Nuclear Power Plant has several stand-alone
computers used for monitoring. Employees log on to these
computers using a local account to verify proper operation
of various processes. The CIO of the organization has
mandated that these computers cannot be connected to the
organization’s network or have access to the Internet.
Which of the following would BEST meet this requirement?
A. Air gap the computers.
B. Place the computers in a screened subnet.
C. Create a separate isolated network for these
computers.
D. Place the computers within a VLAN.
An air gap provides physical isolation, indicating that there is a gap of air between an isolated system and other systems. A screened subnet provides a buffer between the internet and an internal network. Scenario doesn't indicate the computers need to be connected, so a separeate isolated network is not needed

13 C is correct
You have added another router in your network. This router
provides a path to a limited access network that isn’t
advertised. However, a network administrator needs to
access this network regularly. Which of the following could
he do to configure his computer to access this limited
network?
A. Implement QoS technologies.
B. Add a VLAN.
C. Use the route command.
D. Open additional ports on the router.
The route command can be used to display and manipulate the routing table on a Linux computer. Using this you can provide another gateway path through this router to the limited access network. VLAN is used to segment or isolate a network, so configuring one won't grant access to a network. A router doesn't have ports that can be opened for individual users

14 B is correct 
 Several servers in your organization’s screened subnet were
recently attacked. After analyzing the logs, you discover that
many of these attacks used TCP, but the packets were not
part of an established TCP session. Which of the following
devices would provide the BEST solution to prevent these
attacks in the future?
A. Stateless firewall
B. Stateful firewall
C. Network firewall
D. Web application firewall
A stateful firewall filters traffic based on the state of the packet within a session. It would filter a packet that isn't part of an established transmission control protocol (TCP) session, which starts with a TCP three-way handshake. A stateless firewall filters traffic based on the IP address, port, or protocol ID. While it's appropriate to place a network firewall in a screened subnet, a network firewall could be either a stateless firewall or a stateful firewall. A WAF (web application firewall) is only to protect web applications.

15 D and E is correct
Your network currently has a dedicated firewall protecting
access to a web server. It is currently configured with only
the following two rules in the ACL:
PERMIT TCP ANY ANY 443
PERMIT TCP ANY ANY 80
You have detected DNS requests and DNS zone transfer
requests coming through the firewall and you need to block
them. Which of the following would meet this goal? (Select
TWO. Each answer is a full solution.)
A. Add the following rule to the firewall: DENY TCP ALL ALL
53.
B. Add the following rule to the firewall: DENY UDP ALL ALL
53.
C. Add the following rule to the firewall: DENY TCP ALL ALL
25.
D. Add the following rule to the firewall: DENY IP ALL ALL 53.
E. Add an implicit deny rule at the end of the ACL.
The easiest way to add an implicit deny rule at the end of the access control list and all firewalls should have this to block all unwanted traffic. You can also deny all IP traffic using port 53 with DENY IP ALL ALL 53. Domain Name System (DNS) requests use UDP port 53, and DNS zone transfers use TCP port 53, so blocking only TCP 53 or UDP 53 does not block all DNS traffic. Port 25 is for SMTP

# Chapter 4

SSID is the name of the wireless network and disabling the broadcast hides a wireless network from casual users

WPA2 uses AES with CCMP and supports open, preshared key and Enterprise modes

Enterprise mode is more secure than personal mode because it adds authentication and it uses an 802.1X authentication server implemented as a RADIUS server.

WPA3 uses simultaneous authentication of equals (SAE) instead of the PSK. WPA3 supports enterprise mode, similar to WPA2 enterprise mode

WPA3 offers a secure open mode

802.1X servers use one of the Extensible Authentication Protocol (EAP) versions, such as Protected EAP, EAP-Tunneled TLS, EAP-TLS, or EAP-Flexible Authentication via Secure Tunneling

Most secure EAP method is EAP-TLS and it requires a certificate

802.1X server provides strong port security using port-based authentication and it prevents rogue devices from connecting to a network by ensuring only authorized clients can connect

802.1X server provides strong port security using port based authentication

Captive portal forces wireless clients to complete a process, such as acknowledging a policy or paying a access.

Disassociation attack removes a wireless client from a wireless network

Wifi protected setup WPS allows users to easily configure a wireless device by pressing a button or entering a short PIN

Rogue Access point is an AP placed without permission an evil twin is a rogue access point with the same or similar SSID as a legitimate access point

Bluejacking is the practice of sending unsolicited messages to a phone
BlueSnarfing is the unauthorized access to or theft of information from a Bluetooth device
Faraday cages block Bluetooth signals

In wireless replay attacks, an attacker captures data sent between two entities, modifies it, and then impersonates one of the parties by replaying the data. WPA2 and WPA3 are resistant to wireless replay attacks

Network Access Control (NAC) inspects clients for specific health conditions such as up-to-date antivirus software

Agentless NAC system will scan systems remotely instead of installing an agent on the system

Chapter 4 Questions
1. ~~C~~
2. ~~D~~
3. C
4. C
5. ~~D~~
6. ~~D~~
7. ~~D~~
8. C
9. A
10. A
11. ~~C~~
12. B
13. B
14. B
15. ~~A~~

Chapter 4 Question Review

1 B is correct
A HIDS reported a vulnerability on a system based on a
known attack. After researching the alert from the HIDS,
you identify the recommended solution and begin applying
it. What type of HIDS is in use?
A. Network-based
B. Signature-based
C. Heuristic-based
D. Anomaly-based
If the Host-based Intrusion Detection System (HIDS) identified a known issue, it is using signature-based detection. A HIDS is not network-based but a network-based IDS can also use signature detection. Trend based detection systems identify issues by comparing current activity against a baseline. They can identify issues not currently known.

2 C is correct 
You are preparing to deploy a trend-based detection system
to monitor network activity. Which of the following would
you create first?
A. BPDU guard
B. Signatures
C. Baseline
D. Honeypot
A trend based detection system compares current activity with a previously created baseline to detect any anomalies or changes. Signature-based systems use signatures of known attack patterns to detect attacks. A honey pot is a server designed to look valuable to an attacker and can divert attacks

5 B is correct 
Your organization is planning to upgrade the wireless
network used by employees. It will provide encrypted
authentication of wireless users over TLS. Which of the
following protocols are they MOST likely implementing?
A. EAP
B. PEAP
C. WPA2
D. WPA3
Protected Extensible Authentication Protocol can be used for wireless authentication and it uses Transport Layer Security (TLS) to encapsulate and encrypt the authentication conversation within a TLS tunnel. EAP is a basic framework for authentication and can't provide authentication. Neither WPA2 or WPA3 (Wi-fi Protected Access) use TLS.

6 B is correct 
Lisa is creating a detailed diagram of wireless access points
and hotspots within your organization. What is another
name for this?
A. Remote access VPN
B. Wireless footprinting
C. Channel overlap map
D. Architectural diagram
Wireless footprinting creates a detailed diagram of wireless access points and hotspots within an organization, it typically displays a heat map and dead spots if they exist. A remote access VPN provides access to a private network and is unrelated to the question. Wi-Fi analyzers provide a graph showing channel overlaps but not a diagram of wireless access points. An architectural diagram is of a building

7 A is correct 
You are assisting a small business owner in setting up a
public wireless hotspot for her customers. She wants to
allow customers to access the hotspot without entering a
password. Which of the following is MOST appropriate for
this hotspot?
A. Use Open mode.
B. Use a PSK.
C. Use Enterprise mode.
D. Disable SSID broadcast.
Open mode is the best choice of those given for a public wireless hotspot that doesn't require a password. A pre-shared key (PSK) is the same as a password and the scenario says a password isn't desired. Enterprise mode requires each user to authenticate and is typically enabled with a RADIUS server. If you disable service set identifier (SSID) broadcast, it will make it harder for the customers to find the hotspot.

11 A is correct
An attacker can access email contact lists on your
smartphone. What type of attack is this?
A. Bluesnarfing
B. Bluejacking
C. Captive portal
D. WPS
A successful BlueSnarfing attack allows attackers to access data on a smartphone. Bluejacking is the practice of sending unsolicited messages to other Bluetooth devices.

15 D is correct
Your organization recently implemented a BYOD policy.
However, management wants to ensure that mobile devices
meet minimum standards for security before they can
access any network resources. Which of the following would
the NAC MOST likely use?
A. Permanent
B. Health
C. RADIUS
D. Agentless
An agentless NAC system is often used on employee-owned devices and would be appropriate if an organization implemented a bring your own device policy. A permanent network access control agent is installed on the device permanently, but this might cause problems for employee-owned devices. Any NAC agent is a health agent. Remote Authentication Dial In Service (RADIUS) is used for AAA, not to inspect clients.

# Chapter 5

Endpoints are services such as servers, desktops, laptops, mobile devices, or IoT  devices. EDR provides continuous monitoring of endpoints.

TPM - trusted platform module is a chip included with many desktops, laptops, and some mobile devices and it supports full disk encryption, a secure boot process, and supports remote attestation.

Embedded systems are any device that has a dedicated function and uses a computer system to perform that function, an example of such would be a digital camera or a microwave

IoT usually have embedded systems

Supervisory control and data acquisition (SCADA) system controls an industrial control system (ICS)

SCADA and ICS systems are typically in isolated networks without access to the Internet and are often protected by network intrusion prevention systems

a system on a chip (SoC) is an integrated circuit that includes a full computing system

RTOs is a real time OS that reacts within a specific time 

Chapter 5 Questions
1. ~~D~~
2. C
3. D
4. A
5. D (SED stands for Self-encrypting drives)
6. ~~A~~
7. C
8. ~~C~~
9. A
10. ~~D~~
11. A
12. A
13. B
14. ~~D~~
15. ~~C~~

Chapter 5 Questions Review

1 B is correct
Attackers recently exploited vulnerabilities in a web server
hosted by your organization. Management has tasked
administrators with checking the server and eliminating any
weak configurations on it. Which of the following will meet
this goal?
A. Installing a NIDS
B. Disabling unnecessary services
C. Enabling root accounts
D. Implementing SSL encryption
Unnecessary services and open ports are common elements that contribute to weak configurations. A network-based intrusion detection system (NIDS) helps protect internal systems, but a NIDS would not be installed on the server and admins are tasked with checking the server. If root accounts are disabled, enabling them won't increase security. SSL is a **weak encryption protocol** and should **not be used on servers**

6 C is correct 
Managers within your organization want to implement a
secure boot process for some key computers. During the
boot process, each computer should send data to a remote
system to check the computer’s configuration. Which of the
following will meet this goal?
A. Trusted Platform Module
B. Hardware root of trust
C. Remote attestation
D. Tokenization
Remote attestation process checks a computer during the boot cycle and sends a report to a remote system. The remote system attests or confirms that the computer is secure. A Trusted Platform Module (TPM) is a hardware chip on a motherboard and provides a local secure boot process. A TPM includes an encryption key burned into the hardware, which provides a hardware root of trust.

8 B is correct
 Maggie, the new CTO at your organization, wants to reduce
costs by utilizing more cloud services. She has directed the
use of a cloud service instead of purchasing all the
hardware and software needed for an upcoming project.
She also wants to ensure that the cloud provider maintains
all the required hardware and software as a preconfigured
environment where you can deploy your own code. Which
of the following BEST describes the cloud computing service
model that will meet these requirements?
A. IaaS
B. PaaS
C. SaaS
D. XaaS
Platform as a Service (PaaS) provides customers with a preconfigured computing platform including the hardware and software. The cloud platform including the hardware and software. Infrastructure as a Service is a cloud computing option where the vendor provides access to a computer, but customers must install the operating system and maintain the system. Software as a Service provides access to a specific applications such as an email application. Anything as a Service (XaaS) refers to cloud services beyond Iaas, Paas, and SaaS.

10 A is correct 
Your organization has been using more cloud resources and
Lisa, the CIO, is concerned about security. She wants to add
a service that is logically placed between the organization’s
network and the cloud provider. This service will monitor all
network traffic and ensure that data sent to the cloud for
storage is encrypted. Which of the following will BEST meet
these requirements?
A. CASB
B. Storage permissions
C. A storage encryption policy
D. Firewall
A cloud access security broker (CASB) is placed between a network and a cloud provider and would meet the chief information officer (CIO) requirements. It can monitor traffic and enforce security policies, such as ensuring all data sent to the cloud is encrypted. Permissions can't encrypt data. Storage encryption policy can be created to require encryption of data but can't monitor all traffic to and from the cloud. A firewall can't filter traffic.

14 B is correct 
Your organization is switching from a COPE model to a
BYOD model due to the cost of replacing lost or damaged
mobile devices. Which of the following is the BEST choice to
protect the organization’s data when using the BYOD
model?
A. Full-disk encryption
B. Containerization
C. Remote wipe
D. Geolocation
Containerization is the best choice. Organizations can ensure that organizational data is encrypted in some containers without encrypting user data. In a BYOD model organizations typically can't encrypt user data with full-disk encryption. Remote wipe sends a signal to a lost device to erase data, but it won't erase data if the device is damaged, and an attacker may be able to recover data from a damaged device. Geolocation can't protect data.

15 A is correct
Bart is showing Wendell a new app that he downloaded
from a third party onto his iPhone. Wendell has the same
model of smartphone, but when he searches for the app, he
is unable to find it. Of the following choices, what is the
MOST likely explanation for this?
A. Jailbreaking
B. Tethering
C. Sideloading
D. Rooting
Jailbreaking is the most likely reason for this as it is possible to jailbreak an iPhone to remove all Software restrictions, and install software from other places. Tethering is sharing an internet connection. Sideloading is the process of installing application packages from an APK but sideloading isn't relevant in this context. Rooting is done to android deices and provides users root-level access to the device.

# Chapter 6

Nation-state attackers are hired by the govt and unskilled attackers are script kiddies.

Shadow IT refers to unauthorized systems or applications used in an organization without authorization or approval.

All threat actors motivations vary and common attacks include data exfiltration, revenge, monetary gain, war, activism and so on

A worm is self replicating that travels through networks without user intervention. 

A logic bomb executes in response to an event, such as a day, time, or condition. Logic bombs can deliver payloads after the employee has left the company. 

Shoulder surfing is an attempt to gain unauthorized information through casual observation, such as looking over someone's shoulder (side-eye). 

Chapter 6 Questions 
1. B
2. B
3. A (Guess)
4. ~~A~~
5. B
6. A
7. C
8. ~~B~~
9. A
10. ~~D~~
11. C
12. D
13. B
14. D
15. C

Chapter 6 Questions Review 
3 A is correct 
Lisa is a database administrator. She received a phone call
from someone identifying himself as a representative from a
known hardware vendor. He said he’s calling customers to
inform them of a problem with database servers they’ve
sold, but he said the problem only affects servers running a
specific operating system version. He asks Lisa what
operating system versions the company is running on their
database servers. Which of the following BEST describes the
tactic used by the caller in this scenario?
A. Pretexting
B. Tailgating
C. Pharming
D. Smishing

Pretexting is setting up a scenario that has a better chance of getting someone to give him information. If he just asked for the operating system versions on the servers without a prepended scenario, his chance of success would be diminished. Tailgating is the practice of one person following closely behind another to manipulate the DNS name resolution process. Smishing is a form of phishing using text messages.

4 B is correct
Moe is investigating an attack where the attacker seemed to
have information about a computer user who was not
available online. After examining the user’s computer, he
found a small USB device connected between the keyboard
and computer. What has he most likely discovered?
A. Skimmer
B. Keylogger
C. Wiretap
D. Buffer overflow

A keylogger is a hardware device or software program that collects user keyboard activity and reports it back to the attacker. The device in this scenario is a key logger. A skimmer is similar but it collects credit card information, not keyboard activity. A wiretap is a connection made to a telephone or data line to collect network traffic. A buffer overflow attack sends unexpected data to a system to access system memory or cause it to crash. 

8 A is correct 
Homer complained of abnormal activity on his workstation.
After investigating, an administrator discovered his
workstation connects to systems outside the organization’s
internal network using uncommon ports. The administrator
discovered the workstation is also running several hidden
processes. Which of the following choices BEST describes
this activity?
A. Rootkit
B. Backdoor
C. Spam
D. Trojan

A rootkit is typically a hidden processes and it commonly attempts to connect to computers via the Internet. The scenario doesn't address the initial infection. Although an attacker might have used a backdoor to access the user's computer and install the rootkit, backdoors don't run hidden processes. A trojan is malware that looks like it's beneficial, but it is malicious. Spam is unwanted email and is unrelated to this question.

10 B is correct
You are a security professional for the firm that owns the
website getcertifiedgetahead.com. You recently learned that
someone registered the similar domain names
cetcertifiedgetahead.com, and getcertifiedahead.com. What type
of attack should you suspect has taken place?
A. Ransomware
B. Typosquatting
C. Rootkit
D. DNS hijacking

This describes a typosquatting attack where someone buys a domain name that is close to a legitimate domain name, hoping to attract visitors who mistype the original domain. Ransomware typically encrypts data and the attacker then demands payment as ransom, but there isn't any indication that a ransom is requested in this scenario. A rootkit is a program or group of programs that provide root-level access to a system and hides itself to evade detection. There is no evidence of a rootkit here. Finally, DNS hijacking steals traffic for a legitimate domain name by redirecting DNS records. That is not the case in the attack, where a different domain was used. 

# Chapter 7 

DDos attacks are Dos attacks from multiple computers. 

Variants of DDos attacks include reflected attacks, which involve using third-party servers to redirect traffic to the target, and amplified attacks, which combine reflection techniques with amplification to generate an even greater volume of traffic directed at the target.

On-path attacks are a form of interception or active eavesdropping. 

Sophisticated on-path attacks establish secure channels and users may see certificate warnings indicating an on-path attack. SSH will detect a MITM attack

SSL striping converts HTTPS to HTTP

Pharming attack attempts to manipulate the DNS name resolution process by storing incorrect DNS records on a client system.

Secure cookies have an attribute set that instructs web browsers to only send them over encrypted connections, protecting from the from eavesdropping attacks.

Chapter 7 Questions 
1. D
2. A
3. A
4. D
5. A
6. B
7. A
8. A
9. B
10. C
11. D
12. B
13. 