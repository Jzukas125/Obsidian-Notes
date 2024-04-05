#Securityplus 
# Secure Baselines

Secure Baselines
	the security of an application environment should be well defined and all application instances must follow the baseline, such as Firewall settings, patch levels, and OS file versions and may require constant updates
	Integrity measurements check for the secure baseline, should be preformed often, check against well-documented baselines, and failure requires an immediate correction

Establish baselines
	create a series of baselines for foundational security policies
	security baselines are often available from the manufacturer
	Many operating systems have extensive options and there are over 3,000 group policy settings in Windows 10 and only some of those are associated with security

Deploy Baselines
	we now have established detailed security baselines 
	deploy the baselines are usually managed through a centrally administered console
	may require multiple deployment mechanisms 
	automation is the key to deploy to hundreds or thousands of devices

Maintain baselines
	many of these are best practices
	other baselines may require ongoing updates such as a new vulnerability is discovered, an updated application has been deployed, a new operating system is installed
	Test and measure to avoid conflicts and some baselines may contradict others and enterprise environments are complex

Hardening Targets
	no system is secure with the default configurations and some guidelines are needed to keep everything safe
	Hardening guides are specific to the software or platform
	Get feedback from the manufacturer or Internet interest group
	Other general-purpose guides are available online

Mobile devices 
	always connected mobile technologies 
	Updates are critical such as bug fixes and security patches
	Segmentation can protect data and company and user data are separated
	Control with an MDM (mobile device manager)

Workstations
	user desktops and laptops
	constant monitoring and updates like operating systems, applications, and firmware
	Automate the monthly patches and there's likely an existing process
	Connect to a policy management system for an active directory group policy 
	Remove unnecessary software and limit the threats

Network infrastructure devices
	Switches, routers, etc
	Purpose-built devices, like embedded OS, and limited OS access
	Configure authentication 
	Check with the manufacturer like security updates and they are not usually updated frequently

Cloud infrastructure
	Secure the cloud management workstations
	Least privilege, all services, network settings, application rights and permissions
	Configure Endpoint Detection and Response and all devices accessing the cloud should be secure
	Always have backups

Servers 
	Many and varied
	Updates such as operating system updates/service packs, security patches
	User accounts should have minimum password lengths and complexity and account limitations
	Network access and security should limit network access
	Monitor and secure, anti-virus and anti-malware

SACADA / ICS
	Supervisory control and data acquisition system should have large scale, multi-site industrial control systems (ICS)
	PC management equipment like power generation, refining, manufacturing equipment
	Distributed control systems have real-time information and system control
	Requires extensive segmentation and no access from the outside

Embedded systems
	hardware and software designed for a specific function or to operate as part of a larger system
	can be difficult to upgrade 
	correct vulnerabilities and security patches remove potential threats
	Segment and firewall prevent access from unauthorized users

RTOs (Real-time operating system)
	an operating system with a deterministic processing schedule
	no time to wait for other processes 
	devices like industrial equipment, automobiles, and military environments
	Isolate the system and prevent access from other areas
	run with the minimum services and prevent the potential for exploit 
	Use secure communication to protect with a host-based firewall

IoT devices
	weak defaults as IoT manufacturers are not security professionals
	change default passwords
	Deploy updates quickly, can be a security concern
	Segmentation 

# Securing Wireless and Mobile

Site surveys
	determine existing wireless landscape
	identify existing access points 
	work around existing frequencies and layout and plan for interference
	plan for ongoing site surveys 
	Heat maps will identify wireless signal strengths

Wireless survey tools
	signal coverage
	potential interference
	built-in tools
	3rd-party tools
	spectrum analyzer

Mobile Device Management (MDM)
	manage company-owned and user-owned mobile devices 
	Centralized management of the mobile devices 
	Set policies on apps, data, camera, etc and control the remote device and the entire device or a "partition"
	Manage access control and force screen locks and PINs on these single user devices

Bring your own Device (BYOD)
	Employee owns the device and needs to meet the company's requirements
	Difficult to secure as it's both a home device and a work device

COPE 
	corporate own, personally enabled, company buys the device and is used as both a corporate device and a personal device
	Organization keeps full control of the device and is similar to company-owned laptops and desktops
	Information is protected using corporate policies 
	CYOD - choose your own device

Cellular networks
	mobile devices
	Separate land into "cells", antenna coverages a cell with certain frequencies
	Security concerns like traffic monitoring, location tracking, worldwide access to a mobile device

Wi-fi
	local network access 
	same security concerns as other Wi-Fi devices
	Data capture, encrypt your data
	On-path attack can modify and/or monitor data
	Denial of service and frequency interface

Bluetooth
	High speed communication over short distances such as PAN
	Connects our mobile devices and smartphones, tethering headsets and headphones, smartwatches, etc.
	Do not connect to unknown Bluetooth devices and there's formal pairing process to prevent unauthorized connections

# Wireless Security Settings

Securing a wireless network
	an organization's wireless network can contain confidential information
	authenticate the users before granting access
	Ensure that all communication is confidential 
	Verify the integrity of all communication and the received data should be identical to the original sent data 
	A message integrity check (MIC)

The WPA2 PSK problem 
	WPA2 has a PSK brute-force problem
	listen to the four way handshake
	capture the hash and with the hash, attackers can brute force the pre-shared key
	This has become easier as tech improves
	Once you have the PSK, you have everyone's wireless key 

WPA3 and GCMP
	wi-fi protected access 3 
	GCMP block cipher mode and a stronger encryption than WPA2
	GCMP security services has data confidentiality with AES 
	MIC with Galois Message Authentication Code (GMAC)

SAE
	WPA3 changes the PSK authentication process and it includes mutual authentication 
	creates a shared session key without sending that key across the network
	no more four-way handshakes, no hashes, no brute force attacks
	Simultaneous Authentication of Equals and a diffie-hellman derived key exchange with an authentication component
	everyone uses a different session key, even with the same PSK
	An IEEE standard - the  dragonfly handshake

Wireless authentication methods
	gain access to a wireless network
	Credentials like shared password/pre-shared key (PSK)
	configuration part of the wireless network connection can be prompted during the connection process

Wireless security modes
	configure the authentication on your wireless access point / wireless router
	Open system no authentication password is required
	WPA3-Personal / WPa3-PSK 
	WPA2 or WPA3 with a pre-shared key
	everyone uses the same 256-bit key
	WPA3-Enterprise / WPA3-802.1X authenticates users individually with an authentication server

AAA
	Identification - are you who you claim who you are
	Authentication - prove who you say you are
	Authorization - based on your identification and authentication, what access do you have
	Accounting - what resources have you used

Gaining access
![[Pasted image 20240201155539.png]]

RADIUS (Remote Authentication Dial-In User Service)
	one of the more common AAA protocols 
	Supported on a wide variety of platforms and devices
	Centralize authentication for users such as routers, switches, and firewalls, server authentication, remote VPN access, 802.1X network access
	RADIUS services available on almost any server operating system 

IEEE 802.1X
	port based NAT
	don't get access to the network until you authenticate
	used in conjunction with an access database

EAP 
	Extensible Authentication Protocol
	An authentication network
	Many different ways to authenticate based on REC standards
	EAP integrates with 802.1X and prevents access to the network until the authentication succeeds 

IEEE802.1X and EAP
	Supplicant - the client
	Authenticator - the device that provides access
	Authentication server - validates the client credentials

# Application Security

Secure coding concepts
	a balance between time and quality
	programming with security in mind is often secondary
	Testing, Testing, Testing for the QA process
	Vulnerabilities will eventually be found and exploited

Input validation
	what is the expected input, validate actual vs expected
	Document all input methods such as forms, fields, and type
	check and correct all input (normalization)
	a zip code should be only X characters long with a letter in the X column
	Fix any data with improper input
	fuzzers will find what you missed and don't give them an opening

Secure cookies
	cookies are information stored on your computer by your browser
	used for tracking, personalization, session management
	secure cookies have a secure attribute set
	sensitive info should not be saved in a cookie

Static code analyzers
	static application security testing (SAST)
	many security vulnerabilities found easily such as buffer overflows, database injections, etc
	not everything can be identified through analysis like authentication security, insecure cryptography, etc
	Don't rely on automation for everything
	still have to verify each finding and false positives are an issue

Code signing 
	an application is deployed and a users runs application executable or scripts
	so many security questions, has the application been modified in any way, can you confirm that the application was written by a specific developer
	the application code can be digitally signed by the developer 
	Asymmetric encryption
	A trusted CA signs the developer's public key
	Developer signs the code with their private key for internal apps, use your own CA

Sandboxing 
	applications cannot access unrelated resources 
	commonly used during development
	used in many different deployments such as virtual machines, mobile devices, browser iframe, and windows user account control

Application security monitoring
	Real-time information
	View blocked attacks such as SQL injection attempts, patched vulnerabilities
	Audit the logs and find the information gathering and hidden attacks
	Anomaly detection like unusual file transfers and increase in client access

# Asset Management

Acquisition / procurement process
	the purchasing process has multi-step process for requesting and obtaining goods and services
	Start with a request from the user that usually includes budgeting information and formal approvals
	Negotiate with suppliers 
	Purchase, invoice, and payment

Assignment / Accounting
	a central asset tracking system is used by different parts of the organization
	ownership associate a person with an asset and is useful for tracking a system
	Classification is a type of asset, hardware, and software

Monitoring / Asset tracking
	inventory every asset such as laptops, desktops, servers, routers, switches, cables, fiber modules
	Associate a support ticket with a device make and model and can be more detailed than a user's description
	Enumeration - list all parts of an asset and CPU, memory, storage drive, keyboard, mouse
	Add an asset tag such as a barcode, RFID, visible tracking number, organization name

Media sanitization
	system disposal or decommissioning which is completely removing data so no usable information remains
	Different use cases like a clean hard drive for future use or permanently deleting a single file 
	A one-way trip meaning it should be unrecoverable with forensics tools
	Reuse the storage media

Physical Destruction
	Shredder/pulverizer 
	Drill/Hammer
	Electromagnetic (degaussing), removes the magnetic field and destroys the hard drive data and renders the hard drive unusable
	Incineration

Certificate of destruction
	destruction is often done by a 3rd party
	need confirmation that your data is destroyed 
	a paper trail of broken data

Data retention
	backup of your data 
	regulatory compliance - a certain amount of data backup may be required
	Operational needs 
	differentiate by type and application and recover the data you need when you need it 

# Vulnerability scanning

Vulnerability scanning 
	usually minimally invasive unlike a penetration test
	port scan - poke around and see what's open
	identify systems and security devices 
	test from the outside and inside and don't dismiss insider threats
	gather as much information as possible and we'll separate the wheat from the chaff later 

Static code analyzers
	Static Application Security Testing (SAST) helps to identify security flaws
	Many security vulnerabilities found easily such as buffer overflows, database injections, etc.
	Not everything can be identified through analysis and authentication security, insecure cryptography, etc
	Don't rely on automation for everything
	still have to verify each finding as false positives are an issue

Dynamic analysis (fuzzing)
	send random input to an application such as fault-injecting, robustness testing, syntax testing, negative testing
	Looking for something out of the ordinary such as application crash, server error, exception

Fuzzing engines and frameworks
	many different fuzzing options
	very time and processor resource heavy
	many, many different iterations to try and many fuzzing engines use high-probability tests

Package monitoring
	some applications are distributed in a package 
	confirm the package is legitimate such as is it from a trusted source, no added malware, no embedded vulnerabilities
	Confirm a safe package before deployment and verify the contents

# Threat Intelligence 

Threat Intelligence
	research the threats and the threat actors
	data is everywhere
	make decisions based on this intelligence 
	used by researchers, security operations teams, and others

OSINT
	open-source
	Internet, discussion groups, social media
	Government data, mostly public hearings, reports, websites, etc
	Commercial data, maps, financial reports, databases

Proprietary/3rd-party intelligence
	Someone else has already compiled the threat information
	Threat intelligence services
	Constant threat monitoring identifies new threats and create automated prevention workflows

Information-sharing organization 
	public threat intelligence is often classified intelligence 
	private threat intelligence where private companies have extensive resources
	Need to share critical security details has real-time, high-quality cyber threat information sharing
	Cyber Threat Alliance (CTA) - members upload specifically formatted threat intelligence, CTA scores each submission and validates across other submissions and other members can extract the validated data

Dark web intelligence
	Dark web is overlay networks that use the internet and requires specific software and configurations to access 
	Hacking groups and services
	Monitor forums for activity 

# Penetration Testing

Penetration testing
	pertest simulates an attack
	similar to vulnerability scanning except we actually try to exploit the vulnerabilities 
	often a compliance mandate
	NIST Technical Guide to Information Security Testing and Assessment

Rules of engagement 
	An important document that defines the purpose and scope and makes everyone aware of the test parameters
	Type of testing and schedule with on-site physical breach, internal test, external test, Normal working hours, after 6 PM only, etc
	The rules, IP address ranges, emergency contacts, how to handle sensitive information, in-scope and out-of-scope devices or applications

Exploiting vulnerabilities 
	try to break into the system 
	Be careful as this can cause a denial of service or loss of data
	Buffer overflows can cause instability
	Gain privilege escalation
	may need to try many different vulnerability types, password brute-force, social engineering, database injections, buffer overflows, you'll only be sure you're vulnerable if you can by pass security, if you can get through, the attackers can get through

The process
	initial exploitation - get into the network
	lateral movement - move from system to system and the inside of the network is relatively unprotected
	persistence - once you're there, you need to make sure there's a way back in
	Set up a backdoor, build user account, change or verify default passwords
	The pivot - gain access to systems that would normally not be accessible
	Use a vulnerable system as a proxy or relay

Responsible disclosure program
	takes time to fix a vulnerability such as software changes, testing, deployment, etc
	Bug bounty programs, a reward for discovering vulnerabilities, earn money for hacking a system, document the vulnerability to each cash
	A controlled information release, researcher reports the vulnerability, manufacturer creates a fix, the vulnerability is announced publicly

# Analyzing Vulnerabilities

Dealing with false information
	false positives are vulnerabilities that are identified but don't exist
	this is different than a low-severity vulnerability
	False negatives is where a vulnerability exists, but you didn't detect it
	Update to the latest signatures
	Work with the vulnerability detection manufacturer and may need to update their signatures for your environment

Prioritizing vulnerabilities 
	not every vulnerability shares the same priority 
	may be difficult to determine and research has probably already been done
	refer to public disclosures and vulnerability databases, the industry is well versed
	can be found in online discussion groups, and public disclosure mailing lists

CVSS
	Common vulnerability scoring system (CVSS)
	Quantitative scoring of a vulnerability - 0 to 10
	the scoring standards change over time 
	Different scoring for CVSS 2.0 vs CVSS 3.x
	Industry collaboration with enhanced feed and sharing and automation

CVE
	the vulnerabilities can be cross-referenced online
	Common vulnerabilities and exposures (CVE)
	Microsoft security bulletins
	some vulnerabilities cannot be definitively identified and you'll have to check manually to see if a system is vulnerable 

Vulnerability classification
	the scanner looks for everything (meaning signatures)
	application scans such as desktop, and mobile apps
	Web application scans such as a software on a web server
	Network scans and misconfigured firewalls, open ports, and vulnerable devices

Exposure factor
	loss of value or business activity if the vulnerability is exploited usually expressed as a percentage
	A small DDoS may limit access to a service with a 50% exposure factor
	A buffer overflow may completely disable a service with a 100% exposure factor
	A consideration when prioritizing the worst possible outcome probably gets priority

Environmental variables
	what type of environment is associated with this vulnerability
	Prioritization and patching frequency such as a device in an isolated test lab, a database server in the public cloud
	Every environment is different with factors to consider like, the number and type of users, revenue generating application, and potential for exploit

Industry/Organizational Impact
	some exploits have significant consequences and the type of organization is an important consideration
	Tallahassee memorial Healthcare - February 2023 had a ransom ware attack and was closed for two weeks with diverted emergency cases, and had surgeries cancelled

Risk Tolerance
	the amount of risk acceptable to an organization, impractical to remove all risk
	timing of security patches and patching immediately doesn't allow for proper testing
	testing takes time and while you're testing, you're still vulnerable
	there's a middle ground and may change based on the severity

# Vulnerability Remediation

Patching 
	the most common mitigation technique, we know the vulnerability exists, and we have a patch file to install
	scheduled vulnerability/patch notices
	unscheduled patches such as zero days which are often urgent
	Ongoing process and the patches keep coming 

Insurance
	cybersecurity insurance coverage creates lost revenue, data recovery costs, money lost to phishing, and privacy lawsuit costs
	Doesn't cover everything such as intentional acts, fund transfers, etc
	Ransomware has increased popularity of cybersecurity liability insurance and applies to every organization

Segmentation
	limit the scope of an exploit and separate devices into their own networks/VLANS
	A breach would have limited scope 
	Can't patch, disconnect from the world, air gaps may be required
	Use internal NGFWs can block unwanted/unnecessary traffic between VLANS and can identify malicious traffic on the inside

Physical Segmentation
	separate devices

Logical segmentation with VLANS
	Virtual Local Area Networks (VLANs)
	separated logically instead of physically 
	cannot communicate between VLANs without a layer 3 device/router

Compensating controls
	optimal security methods may not be available, can't deploy a patch right now, no internal firewalls
	compensate in other ways, disable the problematic service, revoke access to the application, limit external access, modify internal security controls and software firewalls
	provide coverage until a patch is deployed

Exceptions and exemptions
	removing the vulnerability is optimal but not everything can be patched
	a balancing act can provide the service, but also protects the data and systems
	Not all vulnerabilities share the same severity and may require local login, physical access, or other criteria
	An exception may be an option and usually has a formal process to approve

Validation of remediation
	the vulnerability is now patched 
	rescanning can perform an extensive vulnerability scan
	Audit check remediated systems to ensure and the patch was successfully deployed
	Verification can manually confirm the security of the system

Reporting
	Ongoing checks are required and new vulnerabilities are continuously discovered
	Difficult to manage without automation as manual checks would be time consuming
	Continuous reporting such as the number of identified vulnerabilities, systems patched vs unpatched, new threat notifications, errors, exceptions, and exemptions

# Security Monitoring

Security monitoring
	the attackers never sleep
	monitor all entry points like logins, publicly available services, data storage locations, and remote access
	React to security events with account access, firewall rule base, additional scanning
	Status dashboards can get the status of all systems at a glance

Monitoring Computing resources
	Systems 
		Authentication - logins from strange places
		Server monitoring - service activity, backups, software version
	Applications
		Availability - uptime and response times
		Data transfers - increases or decreases in rates 
		Security notifications - from the developer/manufacturer
	Infrastructure
		Remote access systems - Employees, vendors, guests
		Firewall and IPS reports - increase or type of attack

Log aggregation
	SIEM or SEM (Security information and Event Manager)
	consolidate many different logs to a central database
	Servers, firewalls, VPN concentrators, SANs, cloud services
	Centralized reporting and all information in one place
	Correlation between diverse systems can view authentication and access, can track application access, and measure and report on data transfers

Scanning 
	a constantly changing threat landscape
	new vulnerabilities discovered daily
	many different business applications and services
	systems and people are always moving
	Actively check systems and devices such as operating system types and versions, device driver versions, installed applications, and potential anomalies
	Gather the raw details a valuable database of information

Reporting
	analyze the collected data and create actionable reports
	Status information such as the number of devices up to date/in compliance and devices running older operating systems
	Determine best next steps, a new vulnerability is announced, How many systems are vulnerable?
	Ad hoc information summaries, prepare for the unknown

Archiving
	takes about an average of 9 months for a company to identify and contain a breach
	Access to data is critical and should be archived over an extended period of time
	May have a mandate such as federal law 

Alerting 
	real time notification of security events, causes an increase in authentication errors and large file transfers
	actionable data keeps the right people informed and enables quick response and status information 
	Notifications methods are SMS/text, email, and Security console / SOC

Alert response and remediation
	Quarantine is a foundational security response and can prevent security issues from spreading
	Alert tuning is a balancing act and prevents false positives and false negatives
	An alert should be accurate as this is ongoing process and the tuning gets better as time goes on

# Security Tools

Security Content Automation Protocol (SCAP)
	many different security tools on the market, NGFWs, IPS, vulnerability scanners, etc.
	They all have their own way of evaluating a threat
	Managed by NIST
	Allows tools to identify and act on the same criteria and validates the security configuration, confirms patch installs, and scans for a security breach

Using SCAP
	SCAP content can be shared between tools, focused on configuration compliance and can easily detect applications with known vulnerabilities
	Especially useful in large environments and has many different operating systems and applications 
	This specification standard enables automation
	Automation types has ongoing monitoring, notification and alerting, and remediation of noncompliant systems

Benchmarks
	apply security best-practices to everything such as operating systems, cloud providers, and mobile devices, this is the bare minimum for security settings
	Example: Mobile Device
	- Disable screenshots, disable screen recordings, prevent voice calls when locked, force encryption backups, disable additional VPN profiles, configure a "lost phone" message etc
	Check the center of internet security for popular benchmarks

Agents/Agentless
	check to see if the device is in compliance could install a software agent onto the device and run an on-demand agentless check
	Agents can usually provide more detail by always monitoring for real-time notifications and this must be maintained and updated
	Agentless runs without a formal install, performs the check then disappears, does not require ongoing updates to an agent, will not inform or alert if not running

SIEM
	Logs security events and information
	Log collection of security alerts and has real-time information
	Log aggregation and long-term storage and usually includes advanced reporting features
	Data correlation can link diverse data types

Anti-virus and anti-malware
	anti-virus is the popular term and refers specially to a type of malware
	Malware refers to the broad malicious software category 
	Terms are effectively the same these days
	Make sure your system is using a comprehensive solution

Data Loss prevention
	Where's your data? Social Security numbers, credit card numbers, medical records
	Stop the data before the attacker gets it ie Data Leakage
	So many resources, so many destinations, often requires multiple solutions, endpoint clients, cloud-based systems

SNMP
	Simple network management protocol
	A database of data (MIB) - management information base
	The database contains OIDs - Object Identifiers
	Poll devices over udp/161
	Request statistics from a device like from a server, firewall, workstation, switch, and router
	Poll devices from at fixed intervals and create historical performance graphs

SNMP traps
	most SNMP operations expect a poll and devices then respond to the SNMP request, this requires constant polling
	SNMP trap can be configured on the monitored devices and communicates over udp/162
	Set a threshold for alerts, if the number of CRC alerts increases by 5 send a trap

NetFlow
	gather traffic statistics from all traffic flows
	NetFlow has a standard collection method and many products and options
	Probe and collector - probe watches network communication and summary records are sent to the collector
	Usually a separate reporting app and is closely tied to the collector

Vulnerability scanners
	usually minimally invasive unlike a pen test
	port scan 
	identify systems
	test from the outside and inside
	gather as much info as possible

# Firewalls

Network-based firewalls 
	filter traffic by port number or application, traditional vs NGFW
	Encrypt traffic using VPN between sites
	Most firewalls can be layer 3 devices (routers)
	often sits on the ingress/egress of the network
	Has NAT
	Dynamic routing

Next generation firewalls NGFW
	The OSI application layer like the layer 7 firewall 
	can be called different names, application layer gateway, stateful multilayer inspection, and has deep packet inspection
	Requires some advanced decodes, every packet must be analyzed, categorized, and a security decision determined

Ports and protocols
	make forwarding decisions based on protocol (TCP or UDP) and port numbers, has traditional port-based firewalls and adds to an NGFW for additional security policy options
	Based on destination protocol and port
	Web server: tcp/80, tcp/443
	SSH server: tcp/22
	Microsoft RDP: tcp/3389
	DNS query: udp/53
	NTP: udp/123

Firewall rules
	a logical path and usually top-to-bottom
	can be very general or very specific and specific rules are usually at the top
	Implicit deny and most firewalls include a deny at the bottom
	Access control lists (ACLs) - allow or disallow traffic and has groupings of categories and has source IP, Destination IP, port number, time of day, application

Web server firewall ruleset 

![[Pasted image 20240202124111.png]]

Screened subnet
	an additional layer of security between the you and the internet such as from public access to public resources and private data remains inaccessible

IPS rules
	Intrusion Prevention System and is usually integrated into a NGFW
	different ways to find malicious traffic, looks at traffic as it passes by
	Signature based that looks for a perfect match
	Anomaly-based and builds a baseline of what's normal
	Unusual traffic patterns are flagged

IPS rules 
	you determine what happens when unwanted traffic appears
	thousands of rules 
	Rules can be customized by group or as individual rules
	This can take time to find the right balance

# Web filtering 

Content filtering
	control traffic based on data within the content has URL filtering, and website category filtering
	Corporate control of outbound and inbound data
	Control of inappropriate content such as NSFW
	Protection against evil like anti-virus

URL scanning
	allow or restrict based on Uniform Resource Locator, also called uniform resource identifier (URI), allow list/block list
	Managed by category like auction, hacking, malware, travel, recreation, etc
	Can have limited control and URLs aren't the only way to surf
	Often integrated into an NGFW

Agent based
	install client software on the user's device and is usually managed from a central console
	Users can be located anywhere and the local agent makes the filtering decisions, always-on, always filtering
	Updates must be distributed to all agents such as cloud-based updates, and update status shown at the console

Proxies
	sits between the users and the external network
	receives the user requests and sends the request on their behalf (the proxy)
	useful for caching information, access control, URL filtering, content scanning
	Applications may need to know how to use the proxy (explicit)
	Some proxies are invisible (transparent)

Forward proxy 
	a centralized "internal proxy"
	commonly used to protect and control user access to the internet

Block rules 
	based on specific URL
	category of site content is usually divided into over 50 different topics such as Adult, Educational, Gambling, Govt, Home and garden etc
	Different dispositions such as Educational: allow, Home and Garden: Allow and Alert, Gambling: Block

Reputation
	Filter URLs based on perceived risk 
	Automated reputation and sites are scanned and assigned a reputation
	Manual reputation with managers using admin to assign rep
	Add these dispositions to the URL filter

DNS filtering
	before connecting to a website get the IP address and perform a DNS lookup
	DNS is updated with real-time threat intelligence with both commercial and public lists 
	Harmful sites are not resolved and no IP address, no connection
	This works for any DNS lookup and not just web filtering

# Operating System Security

Active Directory 
	a database of everything on the network such as computers, user accounts, file shares, printers, groups, and more
	Primarily Widows-based
	Manage authentication where users login using their AD credentials 
	Centralized access control and determine which users can access resources
	Commonly used by the help desk that reset passwords, add and remove account

Group policy 
	manages the computers or users with group policies such as local or domain policies and group policy management editor
	A central console with login scripts, network configurations, and security parameters
	comprehensive control with hundreds of configuration controls

Security-Enhanced Linux (SELinux)
	Security patches for the Linux kernel that adds mandatory access control to Linux and  Linux traditionally uses Discretionary Access Control (DAC)
	Limits application access such as least privilege and make a potential breach have a limited scope
	Open source

# Secure Protocols

Unencrypted network data
	network traffic is important
	some protocols aren't encrypted such as telnet, ftp, smtp, imap
	verify with a packet capture, you can view everything over the network
	protocol selection uses a secure application protocol 
	a secure protocol may not be available

Port selection
	secure and insecure application connections may be available
	HTTP and HTTPS, HTTP: port 80, HTTPS: port 443
	port number does not guarantee security 

Transport method
	don't rely on the application needs to encrypt everything over the network transport
	802.11 wireless, open access point: no transport-level encryption while WPA3 encrypts all user data
	VPN creates an encrypted tunnel and all traffic is encrypted and protected and often requires third party services and software

# Email security

Email security challenges
	the protocols used to transfer emails include relatively few security checks
	Spoofing happens all the time
	a reputable sender will configure email validation

Mail gateway 
	the gatekeeper that evaluates the source of inbound email messages, blocks it at the gateway before it reaches the user
	On-site or cloud-based

Sender policy framework (SPF)
	SPF protocol where sender configures a list of all servers authorized to send emails for a domain
	List of authorized mail servers are added to a DNS TXT record and receiving mail servers perform a check to see if incoming mail really did come from an authorized host 

Domain keys identified mail (DKIM)
	a mail server digitally signs all outgoing mail and the public key is in the DKIM TXT record
	the signature is validated by the receiving mail servers and is not usually seen by the end server

DMARC
	Domain-based Message Authentication Reporting, and Conformance (DMARC) which is an extension of SPF and DKIM
	The domain owner decides what receiving email servers should do with emails not validating using SPF and DKIM and that policy is written into a DNS TXT record
	Compliance reports are sent to the email administrator and the domain owner can see how emails are received

# Monitoring Data

FIM (File integrity Monitoring)
	some files change all the time and some files should never change
	monitor important operating system and application files and identify when changes occur
	Windows - SFC (System File Checker)
	Linux - Tripwire
	Many host-based IPS options

Data loss prevention (DLP)
	Looks for system data
	stop the data before attackers get it
	So many sources, so many destinations

Data Loss Prevention systems 
	on your computer has data in use and end point DLP
	on your network has data in motion
	On your serve has data in motion

USB Blocking
	DLP on a workstation will allow or deny certain tasks

Cloud-based DLP
	located between users and the internet and should watch every byte of network traffic
	Block custom defined data strings with unique data for your organization 
	Manage access to URLs and prevent file transfers to cloud storage
	Block viruses and malware and anything traversing the network

DLP and email
	email continues to be the most critical risk vector such as inbound threats, and outbound data loss
	check every email inbound and outbound
	Inbound - block keywords, identify imposters, quarantine email messages
	Outbound - fake wire transfers, W-2 transmissions, employee information

Emailing a spreadsheet template
	November 2016
	Boeing employee email spouse a spreadsheet to use as a template
	contained the personal information of 36,000 Boeing employees
	Boeing sells its own DLP software 

# Endpoint Security

The endpoint
	the user's access has applications and data
	stop the attackers inbound attacks, and outbound attacks
	many different platforms such as mobile and desktop
	protection is multi-faceted 

Edge vs access control
	control at the edge, internet link, managed primarily through firewall rules, firewall rules rarely change
	Access control 
		control from wherever you are depending on the inside or outside
		Access can be based on many rules such as by user, group, location, application, etc
		Access can be easily revoked or changed and security posture can be changed

Posture assessment
	can't trust everyone's computer
	BYOD
	Malware infections
	Unauthorized applications 
	before connecting to the network, perform a health check

Health checks/ posture assessment
	persistent agents can be permanently installed onto a system and periodic updates may be required
	dissolvable agents where no installation is required, runs during the posture assessment, and terminates when no longer required
	Agentless NAC is integrated with active directory, checks are made during login and log off, and can't be scheduled

Failing your assessment
	what happens when it fails
	Quarantine network, notify admins
	Once resolved, try again

Endpoint detection and response
	a different method of threat protection and they should scale to meet the increasing number of threats
	Detect a threat, signatures aren't the only detection tool, behavioral analysis, machine learning, process monitoring, and lightweight agent on the endpoint
	Investigate the threat by root cause analysis
	Respond to the threat by isolating the system, quarantining the threat, rollback to a previous config 
	API driven, no user or technician intervention required

Extended detection and Response (XDR)
	an evolution of EDR that has improved missed detections, false positives, and long investigation times
	Attacks involve more than just the endpoint 
	Add network-based detection to investigate and respond to network anomalies
	Correlate endpoint, network, and cloud data to improve detection rates and simplify security event investigations

User behavior analytics
	XDR commonly includes user behavior analytics extends the scope of anomaly detection
	Watch users, hosts, network traffic, data repositories, etc to create a baseline or normal activity which requires data analysis over an extended period
	Watch for anything unusual and use a set of rules, pattern matching, statistical analysis
	Real-time detection of unusual activity 

# Identity and Access Management 

Identity and Access management (IAM)
	applications are available anywhere such as desktop, browser, mobile devices, etc
	Data can be located anywhere like cloud storage, private data centers, etc
	Many different application users like employees, vendors, contractors, customers
	Give the right permissions to the right people at the right time and prevent unauthorized access

IAM
	Identify lifecycle management as every entity gets a digital identity
	access control 
	Authentication and authorization where entities must prove they are who they claim to be
	identity governance track an entity's resource access and may be a regulatory requirement 

Provisioning/de-provisioning user accounts
	the user account creation process and the account removal process
	provisioning and de-provisioning occurs for certain events like hiring, transfers, promotions, and job separation
	Account details
	An important part of the IAM process

Permission assignments 
	each entity gets limited permissions, just enough to do their jobs, group assignments are common
	Storage and files can be private to that user even if another person is using the same computer
	No privileged access to the operating system, specifically not allowed on a user account

Identity proofing
	IAM process should confirm who I am
	Resolution is who the system thinks you are
	Validation is gathering information from the user
	Verification/Attestation like passport, in-person meeting, etc.
	Automated verification is also an option

Single sign-on (SSO)
	provide credentials one time 
	get access to all available or assigned resources and no additional resources required
	usually limited by time, a single authentication can work for 24 hours, authenticate after the timer expires
	The underlying authentication infrastructure must support SSO which is not always an option

LDAP (Lightweight directory access protocol)
	Protocol for reading and writing directories over an IP network which is an organized set of records, like a phone directory
	X.500 specification was written by the International Telecommunications Union (ITU)
	DAP ran on the OSI protocol stack with LDAP being lightweight
	LDAP is the protocol used to query and update an X.500 directory which is used in windows active directory, Apple OpenDirectory, Novell directory

X.500 distinguished names
	attribute = value pairs
	most specific attribute is listed first and this may be similar to the way you already think

X.500 directory information tree
	hierarchical structure builds a tree
	container objects like country, organization, organizational units 
	Leaf objects like users, computers, printers, files

Security Assertion Markup Language (SAML)
	open standard for authentication and authorization and you can authenticate through a third-party to gain access and one standard does it all, kind of
	Not originally designed for mobile apps and this has been SAML's largest roadblock

The SAML authentication flow 
	![[Pasted image 20240203110004.png]]

OAuth
	authorization framework and determines what resources a user will be able to access
	created by twitter, google, and many others significant industry support
	not an authentication protocol with OpenID connect handles the single sign-on authentication 
	OAuth provides authorization between applications

Federation
	provide network access to others and not just employees but partners, suppliers, and customers
	Provides SSO and more
	Third-parties can establish a federated network can authenticate and authorize between the two organizations, Login with your Facebook credentials 
	third parties must establish a trust relationship and the degree of trust 

Interoperability
	many different ways to communicate with an authentication server
	often determined by what is at hand, we have an LDAP server
	a new app uses OAuth and needs to allow authentication API server
	The interoperability is dependent on the environment and is often part of a much larger IAM strategy

# Access controls

Access controls
	authorization is the process of ensuring only authorized rights are exercised 
	Users receive rights based on access control models 

Least privilege
	rights and permissions should be set to the bare minimum and you only get exactly what's needed to complete your objective
	All user accounts must be limited and applications should run with minimal privileges
	Don't allow users to run with admin privileges and limits the scope of malicious behavior

Mandatory Access Control (MAC)
	the operating system limits the operation on an object based on security clearance levels 
	every object gets a label confidential, secret, top secret, etc
	Labeling of objects uses predefined rules and the admin decides who gets access to what security levels, users cannot change these settings

Discretionary Access Control (DAC)
	used in most operating systems and a familiar access control model
	create a spreadsheet and as the owner, you control who has access 
	you can modify access at any time
	very flexible access control and very weak security

Role-based access control (RBAC)
	you have a role in your organization like a manager, director, team lead, and project manager
	Administrators provide access based on the role role of the user and rights are gained implicitly instead of explicitly 
	In windows, use groups to provide role-based access control

Rule-based access control
	generic term for following rules and conditions other than who you are
	Access is determined through system-enforced rules and system administrators, not users
	The rule is associated with the object system checks the ACLs for that object
	Rule examples: Lab network access is only available between 9 am and 5 PM, only chrome browsers may complete this web form

Attribute-based access control
	users can have complex relationships to applications and data and access may be defined on many different criteria
	ABAC can consider many parameters which is a next generation authorization model
	Combine and evaluate multiple parameters such as resource information, IP address, time of day, desired action, relationship of the data, etc.

Time of day restrictions
	almost all security devices include a time-of-day option can restrict during certain times or days of the week
	usually not the only access control
	Can be difficult to implement especially in a 24-hour environment
	time-of-day restrictions such as training room network is inaccessible between midnight and 6 am, conference room access is limited after 8pm, R&D databases are only after between 8 am and 6 pm

# Multifactor Authentication

Multifactor Authentication
	prove who you are using different methods, a memorized password, a mobile app, and your gps location 
	factors such as something you know, have, are, and where you are

Something you know
	password is a secret word/phrase, or sting of characters and is a very common authentication factor
	PIN - personal identification number and is not typically contained anywhere on smart card or ATM card
	Pattern - complete a series of patterns and only you know the right format

Something you have 
	smart card integrates with devices and may require a pin
	USB security key and a certificate is on the USB device 
	Hardware or software tokens generates pseudo-random authentication codes
	Your phone can get an SMS code

Something you are 
	biometric authentication like fingerprint, iris scan, voice print
	Usually stores a mathematical representation of your biometric and your actual fingerprint isn't usually saved
	Difficult to change 
	Used to very specific situations as its not fool proof

Somewhere you are 
	provide a factor based on your location and the transaction only completes if you are in a particular geography 
	IP address as its not perfect but can help provide more info and works with IPv4, not so much with IPv6
	Mobile device location services  like geolocation to a very specific area and must be in a location that can receive GPS information or near an identified mobile or 802.11 network

# Password Security

Password complexity and length
	make your password strong and resist guessing or brute-force attack
	Increase password entropy and no single words, no obvious passwords, Mix upper and lower case letters, numbers, and special characters
	Stronger passwords are commonly at least 8 characters and these requirements change as processing speed gets faster, consider a phrase or a set of words

Password age and expiration
	password age 
	password expiration where password works for a certain amount of time, system remembers password history, requires unique passwords
	Critical systems might change more frequently like every 15 days or so

Password managers
	important to use different passwords for each account 
	Store all your passwords in a single database that is encrypted, protected and can include multifactor tokens
	Built-in to many operating systems and uses enterprise password managers for centralized management and recovery options

Passwordless authentication
	man breaches are due to poor password control such as weak passwords, or insecure implementation
	Authenticate without a password with ways such as Facial recognition, security key, etc
	Passwordless may not be the primary authentication method

Just-in-time permissions
	in many organizations, the IT team is assigned administrator/root elevated account rights
	Grant admin access for a limited time 
	a breached user account never has elevated rights
	Request access from a central clearinghouse that grants or defines based on predefined security policies
	Password vaulting where passwords are stored in a password vault and the vault controls who gets access to credentials
	Accounts are temporary with just-in-time process creates a time-limited account and admin receives ephemeral credentials

# Scripting and Automation

Scripting and Automation
	automate and orchestrate, don't have to be there, problems solved in your sleep, monitor and resolve problems before they happen
	The need for speed and the script is as fast as the computer 
	Automate mundane tasks

Automation benefits
	save time 
	enforce baselines like missing an important security patch and automatically install when identified
	standard infrastructure configurations, use a script to build a default router configuration
	secure scaling - orchestrate cloud resource, quickly scale up and down, automation ensures power security also scales
	Reaction time, computer is faster than you
	Workforce multiplier, scripting works 24/7

Cases for automation
	user and resource provisioning with on-boarding and off-boarding
	guard rails, a set of automated validations, limit behaviors and responses, constantly check to ensure proper implementation 
	security groups you can assign or remove group access 
	constant audits with human intervention
	Ticket creation automatically identify issues and script email submissions into a ticker
	escalation correct issues before involving a human
	controlling services and access
	continuous integration and testing 
	integrations and application programming interfaces

Scripting considerations
	complexity, many moving parts
	Costs, takes money to script and money to implement
	single point of failure, what happens if it stops working
	technical debt as patching problems may push the issue down the road
	ongoing supportability as the script works greats today but it may not work great tomorrow

# Incident Response

Security incidents
	user clicks an email attachment and executes malware
	DDoS that is executed by a botnet
	confidential information is stolen 
	User installs peer-to-peer software and allows external access to internal servers

NIST SP800-61
	NIST special publication 800-61 revision 2
	Computer security incident handling guide
	Incident response lifecycle: 
		Preparation
		Detection and Analysis
		Containment, Eradication, and Recovery 
		Post-Incident Activity

Preparing for an incident
	communication methods with phones and contact information
	incident handling hardware and software such as laptops, removable media, forensic software, and digital cameras
	Incident analysis resources such as document, network diagrams, baselines, and critical file hash values
	Incident mitigation software such as Clean OS and application images
	Policies needed for incident handling 

The challenge of detection
	many different detection sources with different levels of detail, different levels of perception
	A large amount of "volume" with attacks incoming all the time
	Incidents are almost always complex with extensive knowledge needed

Analysis
	an incident might occur in the future 
	Web server log with a vulnerability scanner in use
	Exploit announcement such as monthly Microsoft patch release
	Direct threats

Analysis
	an attack is underway or an exploit is successful
	buffer overflow attempt is identified by an intrusion detection/prevention system
	Anti-virus software identifies malware, deletes from OS and notifies admins
	Host-based monitor detects a configuration change and constantly monitors system files
	Network traffic flows deviate from the norm and requires constant monitoring

Isolation and containment
	generally a bad idea to let things run their course and an incident can spread quickly 
	Sandboxes - isolated operating system
	Isolation can be sometimes be problematic and malware or infections can monitor connectivity

Recovery after an incident
	get things back to normal, remove the bad, keep the good
	eradicate the bug by removing malware, disable breached user accounts, and fix vulnerabilities
	recover the system and restore the backups, rebuild from scratch, replace compromised files, tighten down the perimeter 

Lessons Learned
	learn and improve
	Post-incident meeting, invite everyone affected by the incident
	Don't wait too long, memories fade over time, some recommendations can be applied to the next event

Answer the tough questions
	what happened exactly?
	How did you incident plans work?
	What would you do differently next time?
	Which indicators would you watch next time?

Training for an incident 
	limited on-the-job training when a security event occurs 
	Train the team prior to an incident with an initial response, investigation plans, incident reporting, and more 
	This can be an expensive endeavor

# Incident Planning

Exercising 
	test yourselves before an actual event 
	use well-defined rules of engagement
	Very specific scenario which is limited to run the 
	evaluate response by documenting and discuss 

Tabletop
	preforming a full-scale disaster drill can be costly and time consuming 
	Many of the logistics can be determined through analysis
	Get a key players together for a table top exercise

Simulation
	test with a simulated event such as a phishing attack, password requests, and data breaches
	Going phishing by creating a phishing email attack, send to your actual user community, and see who bites
	Test internal security and have the phishing get past the filter
	Test the users

Root cause analysis 
	determine the ultimate cause of an incident and find the root cause by asking why
	create a set of conclusions regarding the incident that is backed up by facts
	Don't get tunnel vision and there can be more than a single root cause
	mistakes happen 

Threat Hunting
	The constant game of cat and mouse
	Strategies are constantly changing 
	Intelligence data is reactive 
	Speed up the reaction time

# Digital Forensics

Digital Forensics
	Collect and protect information relating to an intrusion
	RFC 3227 - Guidelines for evidence collection and archiving A good set of best practices
	Standard digital forensic process
	Must be detail oriented

Legal Hold
	A legal technique to preserve relevant information 
	Hold notification 
	Separate repository for electronically stored information (ESI)
	Ongoing preservation 

Chain of custody 
	control evidence that maintains integrity
	everyone who contacts the evidence and uses hashes and digital signatures, and avoids tampering
	Label and catalog everything and digitally tag all items for ongoing documentation 

Acquisition
	Obtain the data using DISK, RAM, firmware, OS files, etc
	Some of the data may not be on a single system like servers, network data, and firewall logs
	For virtual systems, get a snapshot
	Look for any left-behind digital items

Reporting 
	Document the findings for internal use, legal proceedings, etc
	Summary information and the overview of the security event
	Detailed explanation of data acquisition with a step-by-step method of the process
	The findings, an analysis of the data
	Conclusion has the professional results, given the analysis

Preservation
	handling evidence such as isolating and protecting the data and analyzing the data later without any alterations
	manage the collection process, work from copies and manage the data collection from mobile devices
	live collection has become an important skill
	follow best practices to ensure admissibility of data in court

E-discovery
	electronic discovery such as collecting, prepare, review, interpret, and produce electronic documents
	E-discovery gathers data required by the legal process does not generally involve analysis and there's no consideration of intent
	Works together with digital forensics, the e-discovery process obtains a storage drive, data on the drive is smaller than expected, forensics experts determine that data was deleted and attempt to recover the data

# Log data

Security Log files 
	detailed security-related information that is blocked and allowed traffic flows, exploit attempts, blocked URL categories, and DNS sinkhole traffic
	critical security information 

Firewall logs 
	traffic flows through the firewall
	NGFW logs the application used, URL filtering categories, anomalies and suspicious data

Application logs
	specific to the application
	Windows has event viewer/application log
	Linux/macOS has /var/log
	Parse the log details on the SIEM and filter out unneeded info

Endpoint logs
	attackers often gain access to endpoints 
	there's a lot of data on the endpoint
	everything rolls up to the SIEM
	Use with correlation of security events

OS-specific security logs
	OS security events such as monitoring apps, brute force, file changes, and authentication details
	Find problems before they happen such as brute force attacks and disabled services
	May require filtering

IPS/IDS logs 
	Intrusion prevention logs/Intrusion detection system that is usually integrated into an NGFW
	logs contain information about predefined vulnerabilities that have known OS vulnerabilities, generic security events

Network logs
	switches, routes, access points, VPN concentrators and other infrastructure devices 
	Network changes such as routing updates, authentication issues, and network security issues

Metadata
	metadata is data that describes other data sources
	email has header details, sending servers, destination address
	mobile has a type of phone, GPS location
	Web has operating system, browser type and IP address
	Files have names, addresses, phone numbers, and titles

Vulnerability scans
	lack of security controls have no firewall, no anti-virus, and no anti-spyware
	Misconfigurations have open shares and guest accesses
	Real vulnerabilities show especially newer ones and occasionally the old ones

Automated reports
	most SIEMs include a report generator and automate common security reports
	may be easy or complex to create as the SIEM may have its own report generator, and the third party report generators may be able to access the database
	Requires human intervention as someone has to read the reports
	Can be involved to create as the huge data storage and extensive processing time

Dashboards
	real-time status information summarized on a single screen
	add or remove information
	shows the most important data

Packet captures
	solve complex application issues
	gathers packets on the network or in the air
	Very detailed traffic information

