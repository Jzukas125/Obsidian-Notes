#Securityplus 
# Cloud Infrastructures 

Cloud responsibility matrix
	IaaS, PaaS, SaaS, etc
	Security should be well documented and most cloud providers provide a matrix responsibilities 
	These responsibilities can vary from different cloud providers and contractual agreements

Hybrid considerations
	Hybrid cloud has more than one public or private cloud and this adds additional complexity
	Network protection mismatches has authentication across platforms, firewall configurations, and server settings
	Different security monitoring and logs are diverse and cloud specific
	Data leakage where data is shared across the public internet

Third party vendors in the cloud
	ongoing vendor risk assessments are part of an overall vendor risk management policy
	include third-party impact for incident response where everyone is part of the process
	constant monitoring watches for changes and unusual activity

Infrastructure as code
	describe an infrastructure, defines servers, networks, and applications as code
	modify the infrastructure and create versions the same way you version application code
	use the description (code) to build other application instances and build it the same way every time based on the code
	an important concept for cloud computing as it builds a perfect version every time

Server less architecture
	Function as a Service (FaaS) with applications are separated into individual, autonomous functions and remove the operating system from the equation
	Developer still creates the server-side logic can run in a stateless compute container
	may be event triggered and ephemeral and may only run for one event 
	Managed by a third party and all OS security concerns are at the third party

Microservices and APIs
	monolithic applications with one big application that does everything
	application contains all decision making processes such as user interface, business logic, and data input and output
	code challenges include difficulties in a large code base and change control challenges 

Microservices and APIs 
	APIs is an application programming interface 
	API is the glue for the microservices and works together to act as the application
	scalable allows to scale just the microservices that you need
	resilient allows for outages to be contained
	security and compliance are built in as is containment

![[Pasted image 20240130105517.png]]


# Network Infrastructure 

Physical Isolation
	devices are physically separate and give an air gap between switch A and Switch B
	must be connect to provide communication and should establish a direct connection or another switch or router
	Web servers in one rack and database servers on another
	Customer A on one switch, customer B on another with no opportunity for mixing data 

Physical segmentation
	separate devices have multiple devices

Logical Segmentation with VLANs
	Virtual local area networks (VLANs) are separated logically instead of physically and cannot communicate between VLANs without a layer 3 device / router

SDN (software defined networking)
	networking devices have different functional planes of operation such as Data, control, and management planes
	Split the functions into separate logical units which extend the functionality and management of a single device and is perfectly built for the cloud

SDN Layers
	Infrastructure Layer / Data plane - processes the network frames and packets, forwarding, trunking, encrypting, NAT
	Control layer / Control Plane - manages the actions of the data plane, routing tables, session tables, NAT tables, dynamic routing protocol updates
	Application layer / Management plane - configure and manage the device, SSH, browser, API

![[Pasted image 20240130120112.png]]

# SDN Security 

![[Pasted image 20240130120240.png]]


# Other Infrastructure Concepts

Attacks can happen anywhere
	2 categories for IT security, on-premises data is more secure, cloud-based data is more secure
	Cloud-based security is centralized and costs less, no dedicated hardware, no data center to secure and a third party handles everything
	On-premises puts the security burden on the client and the Data center security and infrastructure costs
	Attackers want your data and they don't care where it is

On-premises security
	Customize your security posture and gain full control when everything is in-house
	On-site IT team can manage security better and the local team can ensure everything is secure and a local team can be expensive and difficult to staff
	Local team maintains uptime and availability, system checks can occur at any time and there is no phone call for support
	Security changes can take time such as new equipment, configurations, and additional costs

Centralized vs Decentralized 
	Most organizations are physically decentralized with many locations, cloud providers, operating systems, etc.
	Difficult to manage and protect so many diverse systems can centralize the security management
	A centralized approach has correlated alerts, consolidated log file analysis, and comprehensive system status and maintenance/patching
	not perfect and has single point of failure, potential performance issues

Virtualization
	virtualization can run many different operating systems on the same hardware
	each application instance has its own operating system and adds overhead and complexity
	Virtualization is relatively expensive 

Application containerization
	Container contains everything you need to run an application
	Code and dependencies and a standardized unit of software
	an isolated process in a sandbox is self-contained and apps can't interact with each other
	container image is a standard for portability, lightweight and uses the host kernel and secure separation between applications 


Virtualized vs Containerized
![[Pasted image 20240130134400.png]]

IoT (Internet of Things)
	Sensors like heating and cooling, lighting
	Smart devices 
	Wearable Technology
	Facility automation
	Weak Defaults as IOT manufacturers are not security professionals

SCADA/ICS
	Supervisory Control and Data Acquisition System
	PC manages equipment like with power generation, refining, manufacturing equipment
	Distributed control systems with real-time information and system control
	Requires extensive segmentation and no access from the outside

RTOs (Real-Time Operating System)
	an operating system with a deterministic processing schedule and has no time to wait for other processes, industrial equipment, automobiles, and military environments
	Extremely sensitive to security issues like non-trivial systems, need to always be available, and difficult to know what type of security is in place

Embedded systems
	hardware and software designed for a specific function or to operate as part of a larger system
	is built with only this task in mind and can be optimized for size and/or cost
	Common examples are traffic light controllers, digital watches, and medical imaging systems

High availability
	redundancy doesn't always mean always available and may need to be powered on manually
	HA (high availability) always on, always available
	May include many different component working together and Active/Active can provide scalability advantages
	Higher availability almost always means higher costs, there's always another contingency you could add such as upgraded power, high quality server components, etc

# Infrastructure 

Availability
	System uptime, access data, complete transactions and this is a foundation of IT security
	a balancing act with security and should be available but only to the right people
	We spend a lot of time and money on availability with monitoring, and redundant systems
	An important metric often said as a percentage

Resilience
	eventually something will happen and we need to be able to maintain availability and recover quickly
	based on many different variables there can be a root cause and replacement hardware installation with software patch availability and redundant systems
	Commonly referenced as MTTR which is mean time to repair

Cost
	how much money is required and everything ultimately comes down to cost
	Initial installation is very different across platforms
	Ongoing maintenance is an annual ongoing cost
	replacement or repair costs 
	tax implications has operating or capital expense

Responsiveness 
	Request information 
	Especially important for interactive applications 
	Speed is an important metric and all parts of the application contribute and there's always a weakest link

Scalability
	how quickly and easily can we increase or decrease capacity and this might happen many times a day
	There's always a resource challenge 
	Needs to include security monitoring and increases and decreases as the system scales

Ease of deployment
	an application has many moving parts such as a web server, database, caching server, firewall, etc.
	This might be an involved process and the hardware resources, cloud budgets, change control
	Might be very simple 
	Important to consider during the product engineering phase and one missed detail can cause deployment issues

Risk transference
	many methods to minimize risk and transfer the risk to a third party
	Cybersecurity insurance and attacks and downtime can be covered and are popular with the rise in ransomware
	Recover internal losses and outages and business downtime
	Protect against legal issues from customers and limit the cost associated with legal proceedings

Ease of recovery
	Something will eventually go wrong 
	Malware infection - reloading operating system from original media is 1 hour but reloading from corporate image is 10 minutes 

Patch availability
	software isn't usually static with things such as Bug fixes, security updates, etc
	This is often the first task after installation
	Most companies have regular updates as per micro soft's monthly patch schedule
	Some companies rarely patch which is a significant concern

Inability to patch
	what if patching wasn't an option 
	Embedded systems such as HVAC controls and time clocks
	not designed for end-user updates which is a bit short-sighted
	May need additional security controls such as a firewall for your time clock

Power 
	a foundational element 
	Overall power requirements such as Data center vs. office building
	primary power with one or more providers
	Backup services such as UPS or generators

Compute
	an application's heavy lifting, more than just a single CPU
	the compute engine has more options available in the cloud
	may be limited to a single processor and is easier to develop
	Use multiple CPUs across multiple clouds and additional complexity and enhanced scalability 

# Security Infrastructures 

Device placement
	every network is different and there are often similarities
	Firewalls separate trusted from untrusted and provide additional security checks
	Other services may require their own security technologies, Honeypots, jump server, load balancers, sensors

Security zones
	zone-based security technologies is more flexible than IP address ranges 
	Each area of the network is associated with a zone, trusted untrusted, internal external, inside, Internet, Servers, Databases, Screened
	This simplifies security policies and has 3 categories: Trusted to Untrusted, Untrusted to Screened, Untrusted to Trusted

Attack surface
	how many ways into a building
	everything can be a vulnerability, application code, open ports, authentication process, human error
	minimize the surface audit the code, block ports on the firewall, monitor network traffic in real time

Connectivity
	everything contributes to security including the network connection
	Secure network cabling and protect the physical drops
	application-level encryption meaning the hard work has already been done
	Network-level encryption such as IPsec tunnels, VPN connections

# Intrusion Prevention

Intrusion Prevention system (IPS)
	watches network traffic 
	Intrusions - exploits against operating systems, applications, etc examples include buffer overflows, XSS and other vulnerabilities
	Detection vs Prevention Intrusion detection system (IDS) - Alarm or alert
	Prevention - stop it before it gets into the network

Failure modes
	we hope for 100% uptime which isn't realistic 
	fail open - when a system fails, data continues to flow
	fail closed - when a system fails data does not flow

Device connections
	Active monitoring where the system is connected inline and data can be blocked in real-time as it passes by and Intrusion prevention is commonly active
	Passive monitoring is where a copy of the network traffic is examined using a tap or port monitor and data cannot be blocked in real-time and intrusion detection is commonly passive

Active monitoring
	IDS/IPS sits physically inline and all traffic passes through the IDS/IPS
	Malicious traffic is immediately identified and dropped at the IPS and does not proceed through the network

Passive monitoring
	examine a copy of the traffic with a port mirror (SPAN), network tap
	No way to block/prevent traffic and is common with Intrusion Detection Systems

# Network Appliances 

Jump appliances
	access secure network zones and provides and access mechanism to a protected network
	Highly-secured device could be hardened and monitored
	SSH / Tunnel / VPN to the jump server, RDP, SSH, or jump from there
	A significant security concern such as compromise of the jump server is a significant breach

Proxies
	sits between the users and the external network
	receives the user requests and sends the request on their behalf 
	useful for caching information, access control, URL filtering, content scanning
	applications may need to know how to use the proxy
	some proxies are invisible

Application proxies
	one of the simplest "proxies" is NAT which is a network-level proxy
	most proxies in use are application proxies and the proxy understands the way the application works
	A proxy may only know one application such as HTTP
	many proxies are multipurpose proxies

Forward proxy
	an "internal proxy" is commonly used to protect and control user access to the internet

Reverse Proxy
	inbound traffic from the internet to your internal service

Open proxy
	a third-party, uncontrolled proxy can be a significant security concern and often used to circumvent existing security controls

Balancing the load
	multiple servers 
	invisible to the end-user
	Large-scale implementations like web server farms, database farms
	fault tolerance such as server outages have no effect and have very fast convergence

Active/active load balancing
	configurable load can mange across servers
	TCP offload has protocol overheard
	SSL offload has an encryption/decryption
	caching has fast response
	prioritization has QoS
	content switching has application-centric balancing 
	some servers are active and others are on standby 
	if the active server fails, then the passive server takes its place

Sensors and collectors
	aggregate information from network devices have built-in sensors, separate devices
	integrated into switches, routers, servers, firewalls, etc
	Sensors such as intrusion prevention systems, firewall logs, authentication logs, web server access logs, database transaction logs, and email logs
	Collectors like proprietary consoles (IPS, firewall), SIEM consoles, syslog servers and many SIEMs include a correlation engine to compare diverse sensor data

# Port Security

Port security
	we've created many authentication methods through the years and a network administrator has many choices
	Use a username and password and other factors can be included
	Commonly used on wireless networks and also works on wired networks

EAP
	Extensible Authentication Protocol (EAP)
	Many different ways to authenticate based on RFC standards and manufacturers can build their own EAP methods 
	EAP integrates with 802.1X and prevents access to the network until the authentication succeeds

IEEE 802.1X
	port-based network access control and you can gain access to the network until authenticate
	EAP integrates with 802.1X with 802.1X prevents access to the network until the authentication succeeds 
	Used in conjunction with an authentication database such as RADIUS, LDAP, TACACS+, Kerberos, etc

IEEE 802.1X and EAP 
	Supplicant - the client
	Authenticator - the device that provides access 
	Authentication server - Validates the client credentials 

# Firewall Types

The universal security controls
	standard issue such as home, office, and in your operating system
	control the flow of network traffic and everything passes through the firewall
	Corporate control of outbound and inbound data 
	control of inappropriate content such as NSFW, or parental controls
	Protection against evil and anti-virus and anti-malware

Network-based firewalls
	filter traffic by port number or application such as OSI layer 4 vs OSI layer 7
	Traditional vs NGFW firewalls
	Encrypt traffic and VPN between sites
	Most firewalls can be layer 3 devices and often sits on the ingress/egress of the network
	Network Address Translation functionality 
	Authenticate dynamic routing communication

UTM / All-in-one security appliance
	United threat management (UTM) / Web security gateway
	URL filter/Content inspection
	Malware inspection
	Spam filter
	CSU/DSU
	Router, Switch
	Firewall
	IDS/IPS
	Bandwidth shaper
	VPN endpoint

Next generation firewall (NGFW)
	the OSI application layer and all data in every packet
	Can be called different names and application layer gateway, stateful multilayer inspection, and Deep packet inspection
	Requires some advanced decodes and every packet must be analyzed and categorized before a security decision is determined

NGFWs
	Network-based firewalls 
	Control traffic flows based on the application 
	Intrusion Prevention Systems can identify the application and apply application-specific vulnerability signatures to the traffic
	Content filtering URL filters and control website traffic by category

Web Application Firewalls (WAF)
	not like a normal firewall and applies rules to HTTP/HTTPS conversations
	Allow or deny based on expected input and unexpected input is a common method of exploiting an application
	SQL injection can add your own commands to an application's SQL query
	A major focus of Payment Card Industry Data Security Standard (PCI DSS)

# Secure Communication

VPNs 
	Virtual Private Networks - encrypted data traversing a public network
	Concentrator is an encryption/decryption access device and is often integrated into a firewall
	Many deployment options and is specialized cryptographic hardware and there is many software-based options available 
	Used with client software and is sometimes built into the OS

Encrypted tunnel
	keep data private across the public internet 
	Encrypt your data and add new headers and trailers
	Decrypt on the other side and the original data is delivered 

SSL/TLS VPN (Secure Sockets Layer VPN)
	Uses common SSL/TLS protocol and has almost no firewall issues
	No big VPN clients usually remote access communication 
	Authenticate users no requirement for digital certificates or shared passwords (IPSec)
	Can be run from a browser or from a (usually light) VPN client across many operating systems

SSL/TLS VPN 
	On-demand access from a remote device and software connects to a VPN concentrator 
	Some software can be configured as always-on

Site-to-Site IPsec VPN
	Always-on or almost always
	Firewalls often act as VPN concentrators probably already have firewalls in place

SD-WAN
	software defined networking in a wide area network a WAN built for the cloud
	the data center used to be in one place and the cloud has changed everything
	cloud-based applications communicated directly to the cloud and have no need to hop through a central point

Secure Access Service Edge (SASE)
	Update secure access for cloud services and securely connect from different locations
	Secure Access Service Edge (SASE) a next generation VPN
	Security Technologies are in the cloud that are located close to existing cloud services
	SASE clients on all devices are streamlined and automatic

Selection of effective controls
	many different security options selecting the right choice can be challenging
	VPN and SSL/TLS VPN for user access and IPsec tunnels for site-to-site access
	SD-WAN manage the network connectivity to the cloud and does not adequately address security concerns 
	SASE and a complete network and security solution and requires planning and implementation

# Data Types and Classifications

Data types
	regulated and managed by third-party 
	Government laws and statues
	trade secret an organization's secret formula and often unique to an organization
	intellectual property may be publicly visible such as copyright and trademark restrictions 
	Legal information such as court records and documents, judge and attorney information, PII and other sensitive details, usually stored in many different systems
	Financial information such as internal company financial details, customer financials, payment records, and credit card data, banks records, etc.

Data Types cont
	Human readable - humans can understand the data and very clear and obvious
	Non-human readable - not easily understand by humans, encoded data, barcodes, images
	Some formats are a hybrid

Classifying sensitive data
	not all data has the same level of categorization, license tag numbers vs health records 
	different levels require different security and handling such as additional permissions, a different process to view, restricted network access 

Data classifications
	proprietary - data that is the property of an organization, may also include trade secrets, and often data unique to an organization
	PII - Personally Identifiable Information -- Data that can be used to identify an individual such as Name, date of birth, mother's maiden name, biometric information
	PHI - Protected Health Information -- health information associated with an individual, such as Health status, health care records, payments for health care and much more 

Data classifications 
	Sensitive - intellectual property, PII, PHI
	Confidential - very sensitive, must be approved to view 
	Public / Unclassified - no restrictions on viewing the data
	Private / Classified / Restricted - restricted access, may require an NDA
	Critical - data should always be available

# States of Data

Data at rest
	the data is on a storage device, Hard drive, SSD, flash drive, etc
	Encrypt the data with whole disk encryption, database encryption, file or folder-level encryption
	Apply permissions, access control lists and only authorized users can access the data

Data in transit 
	data transmitted over the network also called data in-motion
	not much protection as it travels like many different switches, routers, devices
	Network-based protection firewall, IPS
	Provide transport encryption such as TLS and IPsec

Data in use 
	Data in actively processing in memory such as system RAM, CPU registers, and cache
	the data is almost always decrypted and otherwise you couldn't do anything with it
	the attackers can pick the decrypted information out of ram 

Data sovereignty 
	data sovereignty is data that resides in a country is subject to the laws of that country 
	Laws may prohibit where data is stored GDPR, Data collected on EU citizens must be stored in the EU, a complex mesh of technology and legalities
	where is your data stored and your compliance laws may prohibit moving data out of the country

Geolocation
	location details and tracks with localized area
	many ways to determine location 
	can be used to manage data access and prevents access from other countries 
	Limit administrative tasks unless secure area is used and permit enhanced access when inside the building 

# Protecting Data

Geographic restrictions 
	network location and identify based on IP subnet and can be difficult with mobile devices
	geolocation - determine a user's location 
	geofencing will automatically allow or restrict access when the user is in a particular location, don't allow this app to run unless you're near the office 

Protecting data 
	primary job task an organization is out of business without data
	data is everywhere, on a storage drive, on the network, in a CPU
	protecting the data like encryption, security policies
	data permissions and not everyone has the same access

Encryption
	encode information into unreadable data, original information is the plaintext and encrypted is ciphertext
	two-way street can convert between one and other if you have the proper key
	Confusion and the encrypted data is drastically different than the plaintext

Hashing 
	represent data as a short string of text, message digest, a fingerprint
	one-way trip is impossible to recover the original message from the digest and is used to store passwords / confidentiality
	verify a download document is the same as the original 
	can be a digital signature 
	will not have a collision

Obfuscation
	obfuscate is to make something normally understandable, very difficult to understand
	Take perfectly readable code and turn it into nonsense and the developer keeps readable code and gives you the chicken scratch, both sets of code perform exactly the same way
	Helps prevent the search for security holes and makes it more difficult to figure out what's happening, but not impossible

Masking 
	a type of obfuscation can hide some of the original data
	Protects PII and other sensitive data
	May only be hidden from view and the data may still be intact in storage
	Control the view based on permissions
	Many different techniques such as substituting, shuffling, encrypting, masking out, etc

Tokenization
	replace sensitive data with a non-sensitive placeholder
	common with credit card processing can use a temporary token during payment and an attacker capturing the card numbers can't use them later 
	Not encryption or hashing and the original data and token aren't mathematically related and there is no encryption overhead

Segmentation
	many organizations use a single data source and one large database
	one large breach puts all of the data at risk
	separate the data and store it in different locations 
	sensitive data should have stronger security and the most sensitive data should be the most secure

Permission restrictions 
	control access to an account, it's more than just username and password
	Determine what policies are best for an organization
	The authentication process such as password policies, authentication factor policies, and other considerations
	Permissions after login are another line of defense and prevent unauthorized access

# Resiliency 

Resiliency - **the ability to recover from setbacks**

High availability
	redundancy doesn't always mean always available and may need to be powered on manually
	HA (high availability)
	May include many different components working together 
	Higher availability almost always means higher cost and there is always another contingency you could add

Server clustering
	combine two or more servers and appears and operates as a single large server and users only see one device
	Easily increase capacity and availability and add more servers to the cluster
	Usually configured in the operating system and all devices in the cluster commonly use the same OS

Load balancing
	load is distributed across multiple servers and the servers are often unaware of each other
	Distribute the load across multiple devices and can be different operating systems 
	The load balancer adds or removes devices and add a server to increase capacity and remove unresponsive servers 

Site resiliency
	recovery site is prepped an data is synchronized
	a disaster is called and a business processes failover to the alternate processing site
	problem is addressed and this can take hours, weeks, or longer
	Revert back to the primary location and the process must be documented for both directions

Hot Site
	an exact replica
	Stocked with hardware that is constantly updated 
	Applications and software are constantly updated 
	Flip a switch and everything moves

Cold site
	No hardware
	No data
	No people

Warm site
	somewhere between cold and hot 
	Big room with rack space 

Geographic dispersion
	sites should be physically different than the organization
	these primary location and many disruptions can affect a large area such as weather events
	can be a logistical challenge such as transporting equipment and getting an employee on-site and getting back to the main office

Platform diversity
	every operating system contains potential security issues that are unavoidable 
	many security vulnerabilities are specific to a single OS
	Use many different platforms such as different applications, clients, and OSes
	Spread the risk around 

Multi-cloud systems
	many cloud providers such as AWS, Microsoft Azure
	Plan for cloud outages 
	Data is both geographically dispersed and cloud service dispersed 
	a breach with one provider would not affect the others 
	Plan for every contingency

Continuity of Operations planning (COOP)
	not everything goes according to plan
	we rely on our computer systems
	there needs to be an alternative such as manual transactions, paper receipts, and phone calls for transaction approvals 
	these must be a documented and tested before a problem occurs

# Capacity planning

Capacity planning 
	match supply to the demand 
	too much demand might cause application slowdowns and outages
	too much supply is wasting money
	requires a balanced approach, add the right amount of people, apply appropriate technology, and build the best infrastructure 

People
	some services require human intervention like call center support lines and technology services
	too few employees, recruit new staff
	too many employees, redeploy to other parts of the organization or downsize

Technology
	pick a technology that can scale and not all services can easily grow and shrink
	Web services distribute the load across multiple web services 
	Database services cluster multiple SQL servers and split the database to increase capacity
	cloud services have services on demand and have seemingly unlimited resources

Infrastructure
	underlying framework like application servers, network services, etc
	Physical devices can purchase, configure, and install
	cloud based devices are easier to deploy and useful for unexpected capacity changes 

# Recovery Testing

Recovery testing 
	test yourselves before an actual event such as scheduled update sessions
	Use well-defined rules of engagement
	Very specific scenario
	Evaluate response, document and discuss

Tabletop exercises
	performing a full-scale disaster drill can be costly and time consuming
	Many of the logistics can be determined through analysis and you don't physically have to go through a disaster or drill
	Get key players together for a tabletop exercise 

Fail over
	a failure is often inevitable and its when and not if
	We may be able to keep running and plan for the worst
	Create a redundant infrastructure 
	If one stops working, fail over to the operational unit and many infrastructure devices and services can do this automatically

![[Pasted image 20240201094005.png]]

Simulation
	test with a simulated event like a phishing attack, password requests, data breaches
	going phishing like creating a phishing email attack, sending to your actual user community, and see who bites 
	test internal security 
	test the users

Parallel processing
	split a process through multiple CPUs, a single computer with multiple CPU cores or multiple physical CPUs
	Improved performance 
	Improved recovery, Quickly identify a faulty system, take the faulty device out of the list of available processors, continue operating with the remaining processors 

# Backups 

Incredibly important
	recover important and valuable data and you should plan for disaster
	Many different implementations all of which account for a total amount of data, a type of backup, backup media, storage location, backup and recovery software, and day of the week

Onsite vs Offsite backup
	On site backups have no internet link required, data is immediately available, and is generally less expensive than off site
	Off site backups can transfer data over internet or WAN link, data is available after a disaster, and restoration can be performed from anywhere
	Organizations often use both which provides more copies of the data and more options when restoring

Frequency
	how often to backup
	this may be different between systems and some systems may not change much each day
	may have multiple backup sets
	this requires significant planning which has multiple backup sets across different days and causes a lot of media to manage

Encryption
	a history of data is on backup media and some of this media may be offsite
	This makes it very easy for an attacker and all of the data is in one place
	Protect backup data using encryption, everything on the backup media is unreadable, and the recovery key is required to restore the data
	Especially useful for cloud backups and storage as it prevents anyone from eavesdropping

Snapshots
	very useful for virtual machines and cloud environments
	Take a snapshot which is an instant backup of an entire system and save the current configuration and data
	Take another snapshot after 24 hours and contains only the changes between snapshots
	Take a snapshot every day revert to any snapshot, allows a very fast recovery

Snapshots
	![[Pasted image 20240201111800.png]]

Recovery testing
	Not enough to perform a backup and you have to be able to restore
	Disaster recovery testing can simulate a disaster situation and restore from backup
	Confirm the restoration and test the restored application and data
	perform periodic audits and always have a good backup, do weekly, monthly, and quarterly checks

Replication
	an ongoing, almost real-time backup and should keep data synchronized in multiple locations
	data is available and there should always be a copy somewhere
	Data can be stored locally to all users and replicate data to all remote sites
	Data is recoverable and disasters can happen at any time

Journaling
	power goes out while writing data to storage and the stored data is probably corrupted 
	Recovery could be complicated, removing corrupted files and restoring from a backup
	Before writing to storage, make a journal entry, after the journal is written, write the data to storage
	After the data is written to storage, update the journal

# Power Resiliency

Power resiliency
	power is the foundation of tech and is important to engineer and plan for outages
	usually don't make our own power and is provided by third parties
	Ways to mitigate power issues

UPS
	Uninterruptible Power Supply (UPS)
	Short-term backup power and helps against blackouts, brownouts, and surges
	UPS types - Offline/Standby UPS, Line-interactive UPS, On-line/Double-conversion UPS
	Features include auto shutdown, battery capacity, outlets, and phone line suppression

Generators
	Long term power backup and require fuel storage
	Power an entire building and some power outlets may be marked as generator-powered
	It may take a few minutes to get the generator up to speed, meaning a  battery UPS should be used while the generator is starting