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
3. ~~A~~
4. D
5. A
6. B
7. A
8. A
9. ~~B~~
10. ~~C~~
11. D
12. ~~B~~
13. C
14. A
15. C

Chapter 7 Questions Review

3 B is correct
An administrator regularly connects to a server using SSH
without any problems. Today, he sees a message similar to
the following graphic when he connects to the server. Which
of the following is the MOST likely reason for this message?
A. Rogue access point
B. On-path attack
C. Cross-site scripting
D. SQL injection

The message indicates a potential on-path attack. Specifically, it indicates that the key on the host system has changed, which may be due to the administrator connecting to the attacking system instead of their true target system. None of the other answers are related to incorrect cryptographic keys. A rogue access point is an unauthorized wireless access point. XSS and SQL injection attacks are attacks against web applications and there are no web applications in use in this scenario.

9 D is correct
Your organization is preparing to deploy a web-based
application, which will accept user input. Which of the
following will BEST test the reliability of this application to
maintain availability and data integrity?
A. Static code analysis
B. Input validation
C. Error handling
D. Dynamic code analysis

Dynamic code analysis techniques test an application during its execution and are the best choice of the available answers to verify the application can maintain availability and data integrity. Static code analysis is done without executing any code, and it won't test its reliability. Input validation is the practice of checking data for validity before using it, but this is done within the application, not as a method to test the application. Error-handling techniques are also done within the application. 

10 D is correct
You are looking for examples of use cases where
automation can improve the efficiency of your security
operations. Which one of the following is NOT a common
automation use case?
A. Ticket creation
B. Incident escalation
C. Continuous integration and testing
D. Vendor evaluation

The common use cases for automation and scripting in security operations are user provisioning, resource provisioning, guardrails, security groups, ticket creation, incident escalation, enabling/disabling services and access, continuous integration and testing, and the use of APIs to create integrations. Vendor evaluation is typically a manual process performed by human analysts and does not commonly benefit from automation. 

12 D is correct 
Looking at logs for an online web application, you see that
someone has entered the following phrase into several
queries: ' or 1=1;--. Which of the following provides the BEST
protection against this attack?
A. Normalization
B. Proper error handling
C. Removing dead code
D. Stored procedures

Attackers commonly use the code in SQL injection attacks, and stored procedures are an effective method of preventing SQL injection attacks. Normalization techniques organize tables and columns in a database to reduce redundant data but don't block SQL injection attacks. 

# Chapter 8 

Credentialed scans run under an account's context and can get more detailed information on targets, such as the software versions of installed applications. They are also more accurate that non-credentialed scans, giving fewer false positives. 

Chapter 8 Questions
1. ~~A~~
2. ~~B~~
3. ~~A~~
4. C
5. ~~C~~
6. D
7. A
8. D
9. ~~B~~
10. C
11. ~~C~~
12. C
13. ~~D~~
14. ~~D~~
15. A

Chapter 8 Questions Review 

1 B is correct 
A server within your organization has suffered six hardware
failures in the past year. IT management personnel have
valued the server at $4,000, and each failure resulted in a
10 percent loss. What is the ALE?
A. $400
B. $2,400
C. $4,000
D. $6,000

Annual loss expectancy (ALE) is 2,400. It is calculated as single loss expectancy (SLE) x annual rate of occurence (ARO). Each failure has resulted in a 10 percent loss. The SLE is 10 percent of $4,000 ($400), and the ARO is 6.6 x $400 is $2400.

2 C is correct 
Maggie is performing a risk assessment on a database
server. While doing so, she created a document showing all
the known risks to this server, along with the risk score for
each risk. Which of the following BEST identifies the name
of this document?
A. Qualitative risk assessment
B. Quantitative risk assessment
C. Risk register
D. Residual risk

A risk register lists all known risks for an asset, such as a database server, and it typically includes a risk score. Risk assessments might be use a risk register, but they are not risk registers. Residual risk refers to the remaining risk after applying security controls to mitigate a risk. 

3 D is correct 
Your organization hosts an e-commerce website used to sell
digital products. You are tasked with evaluating all the
elements used to support this website. What are you
performing?
A. Quantitative assessment
B. Qualitative assessment
C. Threat hunting
D. Supply chain assessment

A supply chain assessment evaluates all the elements used to create, sell, and distribute a product. The NIST RMF provides steps for reducing supply chain risks. Risk assessments evaluate risks, but don't evaluate the supply chain required to support an e-commerce website. Threat hunting is the process of actively looking threats within a network before an automated tool detects and reports on the threat.

5 D is correct
Maggie suspects that a server may be running unnecessary
services. Which of the following tools is the BEST choice to
identify the services running on the server?
A. DNSEnum
B. IP scanner
C. Passive reconnaissance
D. Nmap

Nmap is a network scanner, and it can detect the protocols and services running on a server. The dnsenum command will enumerate Domain Name System (DNS) records for domains. An IP scanner detects IPs active on a network but not the services running on the individual hosts. Passive reconnaissance uses open-source intelligence instead of active tools. 

9 A is correct
Lisa periodically runs vulnerability scans on the
organization’s network. Lately, she has been receiving many
false positives. Which of the following actions can help
reduce the false positives?
A. Run the scans credentialed scans.
B. Run the scans as non-credentialed scans.
C. Run the scans using passive reconnaissance.
D. Run the scans using active reconnaissance.

Running the scans as credentialed scans allows the scan to see more information and typically results in fewer false positives. A false positive indicates the scan reported a vulnerability that doesn't exist. Non-credentialed scans run without any user credentials and can be less accurate. Choosing either passive or active scans won't reduce false positives.

11 D is correct 
Bart, a database administrator in your organization, told you
about recent attacks on the network and how they have
been disrupting services and network connectivity. In
response, he said he has been investigating on his own
using Nmap to run vulnerability scans and identify
vulnerabilities. Which of the following is wrong with this
scenario?
A. The database administrator was pivoting from his
primary job.
B. A network scan wasn’t done first.
C. Scans weren’t done as credentialed scans.
D. Rules of engagement weren’t obtained.

Bart should have gotten authorization before doing any scans, and the authorization should outline the rules of engagement. Pivoting refers to an attacker accessing other systems in network through a single compromised system. While Bart is a database administrator and doing vulnerability scans is outside his normal job functions, his actions wouldn't be described as pivoting. 

13 A is correct
You are reviewing the results of a vulnerability scan and are
having a hard time determining which vulnerabilities to
address first. What standard tool could help you identify the
most severe vulnerabilities?
A. CVSS
B. CVE
C. SCAP
D. MITRE

The common vulnerability scoring system (CVSS) assesses vulnerabilities and assigns severity scores in a range of 0 to 10, with 10 being the most severe. The MITRE corporation maintains the CVE list, which is a dictionary of publicly known security vulnerabilities. The Security Content Automation Protocol is designed to help facilitate communication between vulnerability scanners and other security and management tools.

14 B is correct
Your organization is setting up an e-commerce site to sell
products online. Management wants to ensure the website
can accept credit cards for payment. Which of the following
standards are they MOST likely to follow?
A. ISO 27001
B. PCI DSS
C. ISO 31000
D. SSAE SOC 2 Type I

When using credit cards, a company would comply with the Payment Card Industry Data Security Standard (PCI DSS). International organization for standardization (ISO) 27001 provides information on information security management systems (ISMS) requirements. ISO 31000 is a family of standards related to risk management. A statement on standards related to risk management. A statement on standards for attestation engagements system and organization's systems and covers the design effectiveness of security controls on a specific date. 

# Chapter 9 

RAIDIUS subsystems provide fault tolerance and increase availability. 

Load balancers spread the processing load between servers

Business impact analysis (BIA) is part of a business continuity plan (BCP)

Recovery time objective (RTO) identifies the max amount of time it takes to restore a system

Mean time between failures (MTBF) identifies the average time between failures

A hot site includes everything needed to be operational within 60 minutes and is the most effective recovery solution but it is also the most expensive. 

A cold site has power and connectivity requirements and little else and is the least expensive to maintain. 

Warm sites are a compromise between hot sites and cold sites

DRP is disaster recovery plan

Chapter 9 Questions
1. ~~B~~
2. C
3. ~~C~~
4. A, ~~B~~, C
5. ~~C (guess)~~
6. ~~C~~
7. ~~D~~
8. D
9. D
10. B
11. B
12. ~~A~~
13. ~~A (had to look up)~~
14. ~~B~~
15. ~~A~~

5/15 correct

1 C is correct
 Employees access the data center by entering a cipher code
at the door. However, everyone uses the same code, so it
does not identify individuals. After a recent security incident,
management has decided to implement a key card system
that will identify individuals who enter and exit this secure
area. However, the installation might take six months or
longer. Which of the following choices can the organization
install immediately to identify individuals who enter or exit
the secure area?
A. Access control vestibule
B. Access list
C. CCTV
D. Bollards
E. Compensating control

CCTV can monitor the entrance and record who enters and exits the area. Access list is useful if a guard can identify users and allows access based on the access list itself.

3 B is correct
Which one of the following backup types backs up all of the
data that has changed since the last full backup, and only
the data that has changed since the last full backup?
A. Full backup
B. Differential backup
C. Snapshot backup
D. Incremental backup

A differential backup backs up all of the data that has changed since the last full backup. An incremental backup backs up all of the data that has changed since the last full backup. An incremental backup backs up all of the data that has changed since the last full or incremental backup. A snapshot backup copies all data on the volume being snapshotted. A full backup backs up all data, regardless of what other backups have been performed. 

4 A,C,D 
You need to secure access to a data center. Which of the
following choices provides the BEST physical security to
meet this need? (Select THREE.)
A. Biometrics
B. Cable locks
C. Access control vestibule
D. CCTV
E. HVAC

A biometric reader used for access control, an access control vestibule, and a CCTV system all provide strong physical security for accessing a data center. Cable locks are effective theft deterrents for mobile devices such as laptops, but they don't protect data centers. Heating, ventilation, and air conditioning (HVAC) systems can control the data center's environment, but they don't secure access.

5 D is correct
You need to add disk redundancy for a critical server in your
organization’s screened subnet. Management wants to
ensure it supports a two-drive failure. Which of the
following is the BEST solution for this requirement?
A. RAID-0
B. RAID-1
C. RAID-5
D. RAID-6

A redundant array of inexpensive disks 9 is the best solution of the available answers. It supports a two-drive failure meaning that two drives can fail in the RAID-6, and the disk subsystem will continue to operate. RAID-0 doesn't have any fault tolerance and will fail completely if a single drive fails. Raid-1 only uses two drives. All data is lost if both drives. RAID-5 will continue to operate if one drive fails, but all data is lost if two drives fail.

6 A is correct 
Your organization performs a series of full and incremental
backups. You perform full backups every Sunday evening
and then supplement those with incremental backups on
every evening other than Sunday. Your system fails on a
Thursday morning. What backup should you restore first?
A. Sunday’s full backup
B. Monday’s incremental backup
C. Tuesday’s incremental backup
D. Wednesday’s incremental backup

Because you are performing full and incremental backups, you will need to restore all of these backups. When restoring incremental backups, you always begin by restoring the most recent full backup. In this case, that would be Sunday's backup. You then continue by restoring each of the incremental backups that occurred since that backup, in order from oldest to newest. So you would first restore Sunday's full backup, followed by Monday's incremental backup, Tuesday's incremental backup and, finally, Wednesday's incremental backup.

7 C is correct
You are concerned about the potential loss of backup tapes
while they are in transit to a remote site by a secured
courier. What control can help you protect against the
unauthorized disclosure of confidential information?
A. Maintaining a second set of backup tapes
B. Adding a second courier
C. Encryption
D. All of the above

Encryption protects against the loss of sensitive information. Your goal is to do so here. Adding a second set of tapes or a second courier might reduce the risk of permanently losing the data but those options would not protect against the disclosure of the sensitive information lost on the first set of tables.

12 C is correct 
Your organization hired a security consultant to create a
BIA. She is trying to identify processes that can potentially
cause losses in revenue if they stop functioning. Which of
the following BEST describes what she is identifying?
A. Single points of failure
B. Critical systems
C. Mission-essential functions
D. MTBF

The security consultant is identifying mission-essential functions, which is a key part of a business impact analysis (BIA). A single point of failure is a component within a system that can cause the entire system to fail if the component fails. It's common to eliminate single points of failure of critical systems, but not all single points of failure are supporting mission-essential functions. Critical systems support mission-essential functions. Critical systems points of failure have been eliminated, a critical system can fail but the mission-essential function will continue to operate.

13 B is correct
After a recent attack causing a data breach, an executive is
analyzing the financial losses. She determined that the
attack is likely to result in losses of at least $1 million. She
wants to ensure that this information is documented for
future planning purposes. Which of the following documents
is she MOST likely to use?
A. DRP
B. BIA
C. MTTR
D. RTO

A BIA includes info on potential losses and is the most likely document of those listed where this loss would be documented. A disaster recovery plan includes methods used to recover from an outage.

14 D is correct 
A project manager is reviewing a business impact analysis.
It indicates that a key website can tolerate a maximum of
three hours of downtime. Administrators have identified
several systems that require redundancy additions to meet
this maximum downtime requirement. Of the following
choices, what term refers to the maximum of three hours of
downtime?
A. RPO
B. MTTR
C. MTBF
D. RTO
E. DRP

The recovery time objective (RTO) identifies the maximum amount of time it can take to restore a system after an outage. Because the business impact analysis states that the website can only tolerate three hours of downtime, this also identifies the RTO. The recovery point objective (RPO) identifies a point in time where data loss is acceptable, but it doesn't refer to downtime. The mean time to repair (MTTR) metric identifies the average time it takes to restore a failed system, but not a maximum amount of time a system can be down. The mean time between failures (MTBF) metric provides a measure of a system's reliability and is usually represented in hours. A disaster recovery plan (DRP) details the recovery steps to take after different types of disasters.

15 B is correct
Lisa has scheduled quarterly meetings with department
leaders to discuss how they would respond to various
scenarios such as natural disasters or cyberattacks. During
the meetings, she presents a scenario and asks attendees
to indicate their responses. Also, during the meetings, she
injects variations on the scenario similar to what may
happen during a live event and encourages attendees to
discuss their responses. What does this describe?
A. Simulation
B. Tabletop exercise
C. Incident response
D. Testing site resiliency

This is a tabletop exercise. A tabletop exercise is discussion-based, and participants discuss their responses to various scenarios. A simulation is a hands-on exercise, not a meeting. 

# Chapter 10 

Hashing retains integrity 

Spraying attack attempts to by pass account lockout policies. An automated program starts with a large list of targeted user accounts.

Pass the hash attack can allow attackers to log in using the hash of the password without knowing the password

Block ciphers encrypt data in fixed-size blocks. Advanced Encryption Standard (AES) encrypts data in 128-bit blocks and 3DES encrypts data in 64-bit blocks

Stream ciphers encrypt data 1 bit or 1 byte at a time

PKI is public key infrastructure 

CRL is certificate revocation list

Chapter 10 Questions
1. B
2. ~~D~~
3. D
4. B
5. A
6. ~~D~~
7. ~~A~~
8. ~~A~~
9. ~~A~~
10. ~~B~~
11. ~~B~~
12. ~~A~~
13. D
14. ~~B~~
15. ~~D~~~~
5/15

2 A is correct
Users in your organization sign their emails with digital
signatures. Which of the following provides integrity for
these digital signatures?
A. Hashing
B. Encryption
C. Non-repudiation
D. Private key

Hashing provides integrity for digital signatures and other data. A digital signature is a hash of the message encrypted with the sender's private key, but the encryption doesn't provide integrity. The digital signature provides non-repudiation, but non-repudiation does not provide integrity. The private and public key are both needed, but the private key does no provide integrity.

6 A is correct 
A developer is creating an application that will encrypt and
decrypt data on mobile devices. These devices don’t have a
lot of processing power. Which of the following
cryptographic methods has the LEAST overhead and can
provide encryption for these mobile devices?
A. Elliptic curve cryptography
B. Perfect forward secrecy
C. Salting
D. Digital signatures

Elliptic curve cryptography has minimal over head and is often used with mobile devices for encryption. Perfect forward secrecy refers to session keys and provides assurances that session keys will not be compromised even if a private key is later compromised. Digital signatures provide integrity, authentication, and non-repudiation, not encryption.

7 C is correct
You are configuring a web server that will be used by
salespeople via the Internet. Data transferred to and from
the server needs to be encrypted, so you are tasked with
requesting a certificate for the server. Which of the following
would you MOST likely create to request the certificate?
A. CA
B. CRL
C. CSR
D. OCSP

You would request a certificate by creating a certificate signing request (CSR). It uses a specific format to request a certificate. You submit the CSR to a certificate authority (CA), but the request needs to be in the CSR format. A certificate revocation list (CRL) is a lost of revoked certificates. The Online Certificate Status Protocol (OCSP) is an alternate method of validating certificates and indicates if a certificate is good, revoked, or unknown.

8 B is correct
 Users within an organization frequently access public web
servers using HTTPS. Management wants to ensure that
users can verify that certificates are valid even if the public
CAs are temporarily unavailable. Which of the following
should be implemented to meet this need?
A. OCSP
B. CRL
C. Private CA
D. CSR

A certificate revocation list (CRL) can meet this need because CRLs are not cached. If the public certificate authority (CA) is not reachable due to any type of connection outage or CA outage, the cached CRL can be used if the cache time has not expired. The online certificate status protocol works in real-time where the client queries the CA with the serial number of the certificate. If the CA is unreachable, the certificate cannot be validated. A private CA is used within an organization and cannot validate certificates from a public CA. You request a certificate with a certificate signing request (CSR), but the CSR doesn't validate an issued certificate. 

9 D is correct 
Your organization hosts an internal website used only by
employees. The website uses a certificate issued by a
private CA and the network downloads a CRL from the CA
once a week. However, after a recent compromise, security
administrators want to use a real-time alternative to the
CRL. Which of the following will BEST meet this need?
A. SAN
B. CSR
C. RA
D. OCSP

The Online Certificate Status Protocol (OCSP) provides real-time responses to validate certificates issued by a certificate authority (CA). A certificate revocation list (CRL) includes a list of revoked certificates, but it is only downloaded once a week, it can quickly be out of data. None of the other answers validates certificates. In the context of certificates, a subject alternative name (SAN) certificate is used for multiple domains that have different names but are owned by the same organization. A certificate signing request (CSR) is used to request a certificate. A registration authority (RA) accepts CSRs for a CA.

10 C is correct.
An organization hosts several web servers in a web farm
used for e-commerce. Due to recent attacks, management
is concerned that attackers might try to redirect website
traffic, allowing the attackers to impersonate their ecommerce site. Which of the following methods will address
this issue?
A. Stapling
B. Perfect forward secrecy
C. Pinning
D. Key stretching

Certificate pinning provides clients with a list of public key hashes that clients can use to detect website impersonation attempts. Stapling reduces Online Certificate Status Protocol (OCSP) traffic by appending a timestamped, digitally signed OCSP response to a certificate. Perfect forward secret ensures that the compromise of one session key does not compromise other session keys used in the past. Key stretching techniques add additional bits to passwords, make them harder to crack. 

11 D is correct 
Management has mandated the use of digital signatures by
all personnel within your organization. Which of the
following use cases does this support?
A. Supporting confidentiality
B. Supporting availability
C. Supporting obfuscation
D. Supporting non-repudiation

Digital signatures will support a use case of supporting non-repudiation. Digital signatures also provide integrity and authentication, but these weren't available answers. Digital signatures don't encrypt, so they do not support a use case of supporting confidentiality. Redundancy and fault tolerance solutions will increase availability. 

12 D is Correct 
A DLP system detected confidential data being sent out via
email from Bart’s account. However, he denied sending the
email. Management wants to implement a method that
would prevent Bart from denying accountability in the
future. Which of the following are they trying to enforce?
A. Confidentiality
B. Encryption
C. Access control
D. Non-repudiation

Non-repudiation methods such as digital signatures prevent users from denying they took action. If a data loss prevention (DLP) system detected the outgoing email and it was signed with Bart's account using a digital signature, he couldn't believable deny sending it. 

14 A is correct 
You are tasked with getting prices for certificates. You need
to find a source that will provide a certificate that can be
used for multiple domains that have different names. Which
of the following certificates is the BEST choice?
A. SAN
B. Domain validation
C. Extended validation
D. Wildcard

A subject alternative name (SAN) certificate is used for multiple domains that have different names but are owned by the same organization. A domain-validated certificate indicates that the certificate requestor has some control over a Domain Name System domain. Extended validation certificates use additional steps beyond domain validation. 

15 B is correct
Your organization recently lost access to some decryption
keys, resulting in the loss of some encrypted data. The chief
information officer (CIO) mandated the creation of a key
escrow. Which of the following cryptographic keys are MOST
likely to be stored in key escrow?
A. Public
B. Private
C. Ephemeral
D. Session

Copies of private keys are typically stored in a key escrow so that data encrypted with a private key can be retrieved if the original private key is no longer accessible. 

# Chapter 11

Tabletop exercises are a type of scenario-based training where participants discuss and analyze a hypothetical incident in a non-threatening environment. 

When collecting evidence ensure that it is admissible in court. 

Chain of custody provides assurances that personnel controlled and handled evidence properly after collecting it.

Legal hold refers to a legal obligation to maintain different types of data as evidence. Electronic discovery, or eDiscovery, is the identification and collection of electronically stored information. A legal hold requires an organization to protect existing data as evidence.

Investigators provide a report on their findings. They typically include tactics, techniques, and procedures used by attackers and recommendations based on the results

Security goverance is the set of responibilities and processes established by an organization's top-level management to direct, evaluate, and control the organization's security efforts.