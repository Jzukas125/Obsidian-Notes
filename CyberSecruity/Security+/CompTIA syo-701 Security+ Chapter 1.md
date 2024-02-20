These next few chapters of cyber security will be covering the Professor Messer YouTube video series found [here](https://www.youtube.com/watch?v=KiEptGbnEBc&list=PLG49S3nxzAnl4QDVqK-hOnoqcSKEIDDuv)
# Security Controls

Control Types fit into control categories such as firewall being a preventive control type that is a technical control

Control Categories 
	Technical Controls - Controls implemented using systems, operating system controls, firewalls, antivirus
	Managerial Controls - Administrative controls associated with security design and implementation, Security policies
	Operational Controls - Controls implemented by people instead of systems, i.e. Security guards
	Physical Controls - Limits Physical Access, i.e. Guard shack

Preventive Control Type - Blocks Access, i.e. firewall rules, guard shack checking ID

Deterrent Control Type - Discourages an intrusion attempt, does not directly prevent, i.e. warning signs (physical), threat of demotion (managerial)

Detective Control Type - Identify and log an intrusion attempt, may not prevent, i.e. collects and reviews system logs, reviews login reports

Corrective Control Type - Apply a control after an event has been detected, reverses the impact of an event, i.e. restoring from backups can mitigate a ransomware infection

Compensating - control by using other means, existing controls aren't sufficient, prevent the exploitation of a weakness, i.e. firewall blocks a specific application instead of patching it

Directive Control Types - Direct a subject towards a security compliance, relatively weak security control, i.e. store all sensitive files in a protected folder or create compliance policies and procedures

Some organizations may combine types 

# The CIA Triad
Combination of basic security principles 
Confidentiality - certain information should only be known to certain people

Integrity - Data is stored and transferred as intended 

Availability - Information is accessible to authorized users

# Non-repudiation
Similar to signing a contract, signature adds non-repudiation

Proof of integrity
	Verifies data does not change, so the data remains accurate and consistent
	In  cryptography a hash is used 
	Doesn't associate with an individual 
	It allows the hashes to be compared for data to see if anything changed 

Proof of Origin 
	will sometimes be called authentication
	Uses a private key, that gets verified with the public key


# AAA Framework

Identification - Is this who you actually are
Authentication - Prove you say who you are
Authorization - What access do you have
Accounting - Resources used: Login time, data sent and received, logout time

Authentication 
	Have to manage multiple devices
	Systems can't type passwords
	Will have to put a digital signature on the device
	Other business processes rely on this certificate 

Authorization Model
	What can they access
	Users and Services -> data and applications
	Put an authorization model in the middle, define by roles, organizations, attributes, etc


# Take https://www.examcompass.com/comptia-security-plus-practice-test-1-exam-sy0-701 to practice these topics so far

# Gap Analysis 
 is a study of where we are and where we need to be
Usually takes weeks, months, or years and uses emails, data gathering, and technical research

Get a baseline of employees
	Of which includes formal experience, current training, and knowledge of security policies 
	Examine the current processes, which is researching existing IT systems and evaluating existing security policies

Compare and Contrast 
	Compare existing systems
	Identify weaknesses as well as the most efficient processes 
	A detailed analysis should examine broad security categories and break those into smaller segments

Analysis and Report
	The final comparison has a detailed baseline objectives and a clear view of the current state
	It also plans a path to get from where we are to where we need to be which includes time, money, and lots of change control
	This is usually done in a formal description of the current state and has recommendation on how to meet the baseline


# Zero Trust
Many networks are open once the firewall is bypassed
	Newer networks are changing to be zero trust with zero trust meaning that nothing is trusted, using MFA, encryption, systems permissions, more firewalls, and etc. to keep security.

Planes of Operation
	Split the network into functional planes which applies to physical, virtual, and cloud components. Can be looked as having two different planes of operation
	Data plane - processes frames, packets, and network data while 
	Control plane - manages actions of the data plane, defines policies and rules, and determines how packets should be forwarded

Example
![[Pasted image 20231223130930.png]]


Controlling Trust
	Adaptive identity is considering the source of the requested resources, multiple risk indicators - relationship to the organization, physical location, type of connection, IP address. Make the authentication stronger if needed.
	Threat scope reduction could then decrease the number of possible entry points
	Policy-driven access control then combines the adaptive identity with a predefined set of rules.

Security Zones
	Security Zones look at where they are connecting from and checks for trusted, untrusted, internal network, external, VPN 1, VPN 5, VPN 11, marketing, accounting, etc.
	Using the zones may be enough by itself to deny access while some zones are implicitly trusted.

Policy Enforcement Point 
	Allows for these policies to be created and used
	It affects subjects and systems which are commonly end users, applications, and non-human entities with the Policy enforcement point is the gatekeeper.

Applying Trust in the planes
	Policy Decision Point decides the process for making authentication decisions 
	Policy Engine evaluates each access decision based on policy and other information, decides to grant, deny, or revoke
	Policy Administrator communicates with the policy enforcement point and generates access tokens or credentials, and tells the PEP to allow or disallow access.


# Physical Security 

Barricades
	Prevents access
	Channels people through certain a specific access point, prevents cars

Access Control Vestibules
	Extra room you need to pass through
	All doors normally unlocked, while opening one causes others to lock
	All doors normally locked and unlocking one door prevents others from being unlocked
	One door open / others locked when one is open the others cannot be unlocked
	One at a time, controlled groups with a managed control through an area

Fencing
	Builds a perimeter
	Transparent or opaque 
	Would like it to be hard to cut through
	Could prevent climbing with height or razor wire

Video Surveillance 
	CCTV (closed circuit television) can replace physical guards
	Features include motion recognition and object detection 

Guards and Access Badges 
	Security guard allows for physical protection at the reception area and validates identification of existing employees
	Two-person integrity minimizes exposure to an attack and no single person has access to a physical asset
	Usually has access badges with a picture, name, and other details, with it must being worn at all times, and being electronically logged

Lighting
	More lights means more security as people avoid lights, easier to see, non IR can see better
	Specialized design must fit the area 

Sensors
	Infrared detects infrared radiation in both light and dark, common in motion sensors
	Pressure sensors may also be used
	Microwave detects movement across a large area
	Ultrasonic sends ultrasonic signals, receive reflected sound waves

# Deception and Disruption 

Honey Pots
	Attract the bad guys and trap them there
	The "attacker" is usually a machine, and we are trying to see what automation they're using 
	Honeypots create a virtual world to explore

Honeynets
	A real network includes more than a single device 
	May consist of servers, workstations, routers, switches, and firewalls
	Honeynets build a larger deception network with one or more honeypot

Honeyfiles
	Attract attackers with more honey by creating files with fake information
	Honeyfiles have bait for the honeynet and add many honeyfiles to file shares
	an alert is sent if the file is accessed basically a virtual bear trap

Honeytokens
	track malicious actors and add some traceable data to the honeynet
	API credentials does not provide access and sends a notif when used
	Fake email addresses are added to a contact list 
	Many other examples such as database records, browser cookies, and web page pixels

# Change Management

Change management
	includes how to make a change with is upgrading software, patching applications, changing firewall configurations, and modifying switch ports
	One of the most common risks as it occurs very frequently
	Often overlooked or ignored

Change approval Process
	A formal process for managing change that avoids downtime, confusion, and mistakes
	Follows a typical approval process that requires request forms, determining the purpose of the change, identify the scope of the change, scheduling a date and time of the change, determine affected the risk associated with the change, getting approval from the change control board, and get end-user acceptance after the change is complete.

Ownership
	An individual or entity needs to make the change, they own the process, they don't perform the actual change
	The owner managers the process, process updates are provided to the owner, ensures the process is followed, and acceptable
	Address label printers needs to be upgraded, shipping and receiving department owns the process, IT handles the actual change

Stakeholders 
	Usually impacted by this change, 
	impact may not be as obvious as you might think

Impact analysis
	Determine a risk analysis
	Risks can be minor or far-reaching 
	Need to analyze risk for not making the change

Test results 
	May use a sandbox test environment to upgrade, apply the patch
	Confirm a back out plan that will allow everything to be restored

Backout Plan
	Changes don't always work and need to be reverted 
	Always have a backup plan

Maintenance Window
	Consider the frame of time for updates 
	Overnights are a better choice 
	Time of year may be a consideration as retail networks are frozen during the holiday season

Standard Operating Procedure
	Change management affects everyone in the organization
	Process must be well documented and should be available on the intranet
	Changes to the process are reflected in the standards 

# Technical Change Management

TCM
	Put the change management process into action and execute the plan
	No such thing as a simple upgrade as they have many moving parts
	Change management cares more about what to change, and the technical team is concerned about how to change it

Allow/Deny list
	Allow list denies anything that isn't allowed, very restrictive
	Deny list denies anything on the list, antivirus, anti-malware

Restricted Activities
	Scope of change is important
	Change approval isn't permission to make any change
	scope may need to be expanded during the change window
	change management process determines the next steps

Downtime
	Services will be unavailable
	If possibly prevent downtime by switching to a secondary system
	Minimize any downtime events by automating and switching to a secondary is issues appear 
	Send emails and calendar updates

Restarts
	Common to require a restart
	stop and restart the service or daemon
	close the application completely to restart

Legacy applications 
	Very old and will be used after your death
	Often no longer supported by the developer as you are now the support team
	Needs documentation
	Create specific processes and procedures 
	Become the expert

Dependencies
	Service will not start without other active services
	Modifying one component may require changing or restarting other components
	Dependencies may occur across systems, upgrade  the firewall code first then upgrade the firewall management software

Documentation
	Can be hard to keep up as it needs to be updated constantly to avoid being outdated
	Updating diagrams 
	Updating policies/procedures

Version Control
	Track changes to a file or configuration to a file or configuration data over time 
	Many opportunities to manage versions such as, router configurations, window OS patches, application registry entries
	Not always straightforward, some devices and OS's provide version control features and may require additional management software

# Public key Infrastructure 

PKI
	Policies, procedures, hardware, software, people
	Digital Certificates: create, distribute, manage, store, and revoke
	Lots of planning involved
	Also refers to the binding of public keys to people or devices

Symmetric Encryption
	A single shared key that is used to encrypt or decrypt with the same key
	Secret Key algorithm
	Doesn't Scale well
	Very fast to use and has less overhead than asymmetric encryption

Asymmetric Encryption
	Public key cryptography, two or more mathematically related keys
	Private Key 
	Public key, anyone can see this key
	Private key is the only key that can decrypt data encrypted with the public key

The Key pair
	Asymmetric encryption
	Key generation as it builds both public and private key at the same time
	Lots of randomization
	large prime numbers
	lots of math
	Everyone can have public key

![[Pasted image 20240124084757.png]]

Key Escrow
	Someone else holds your decryption keys
	Your private keys are in the hands of a 3rd party
	May be within your own organization
	Can a legitimate business arrangement
	Business might need access to employee information
	government agencies may need to decrypt partner data
	Highly debated but still may be required

# Encrypting Data

Encrypting stored data
	Protect data on storage devices such as SSD, hard drive, USB drive, cloud storage etc.
	Full disk and partition/volume encryption such as BitLocker, File Vault, etc.
	File Encryption, EFS, third party utilities

Database Encryption
	Protecting stored data and the transmission
	Transparent encryption, encrypt all database information with a symmetric key
	Record-level encryption, encrypts individual columns, and use separate symmetric keys for each column

Transport Encryption
	Protect data traversing the network 
	Encrypting in the application and browsers can communicate using HTTPS
	VPNs, encrypt all data transmitted over the network, regardless of the application
	IPsec for site-to-site

Encryption Algorithms
	Many, many different ways to encrypt data
	Proper formula must be used during the encryption and decryption process
	Both sides decide on the algorithm before encrypting the data, details are often hidden from the end user
	Advantages and Disadvantages between algorithms, such as security level, speed, and complexity

Cryptographic Keys
	Very little that isn't known about the cryptographic process
	Algorithm is usually a known entity and the only thing you don't know is the key
	The key determines the output for encrypted data, hash value, digital signature

Key lengths
	Larger keys tend to be more secure, as they prevent brute force attacks and attackers can try every possible key combination
	Symmetric encryption, 128-bit or larger symmetric keys are common, these numbers get larger as time goes on
	Asymmetric encryption, complex calculations of prime numbers, larger keys than symmetric encryption, common to see key lengths of 3,072 bits or larger

Key stretching 
	A weak key is a weak key 
	Make a weak key stronger by performing multiple processes such as hashing a password, hashing the hash of the password and so on
	Brute force attacks would require reversing each of those hashes

# Key Exchange

Key Exchange
	A logistical challenge
	Out of band key exchange, don't send it online
	In-band key exchange, it's on the network, protect key with additional encryption
	Use asymmetric encryption to deliver a symmetric key

Real-time Encryption/decryption
	Need for fast security
	share a symmetric session key using asymmetric encryption
	Implement session key carefully

![[Pasted image 20240124091559.png]]

# Encryption Technologies

Trusted Platform Module (TPM)
	specification for cryptographic functions
	cryptographic processor, random number generators, key generators
	persistent memory with unique keys burned in during manufacturing
	Versatile memory, storage keys hardware configuration information, securely store bit locker keys 

Hardware Security Module (HSM)
	Used in large environments, clusters, redundant power 
	High-end cryptographic hardware, plug in card or separate hardware device
	Cryptographic accelerators that offload CPU overhead from other devices

Key management System
	Services are everywhere, such as on-premises or cloud based
	Manage all keys from a centralized manager that are often provided as third party software
	 Separate the encryption keys from the data 
	All key management from one console, create keys for a specific service or cloud provider and associate keys with specific users, rotate keys on regular intervals, and log key use and important events

Keeping data private
	data is located everywhere on every device imaginable
	Most private data is usually closest to us
	data is constantly changing

Secure Enclave
	protected area for our secrets that is often implemented as a hardware processor and is isolated from the main processor and has many different tech and names
	provides extensive security features, has its own boot ROM, monitors the system boot process, true random number generator, and has real-time memory encryption, has root cryptographic keys, performs AES encryption in hardware


# Obfuscation

Obfuscation
	process of making something more difficult to understand but not impossible to read if you know how to
	Hiding information in plain sight
	Steganography 

Steganography
	Security through obscurity
	message is invisible but still there

Common techniques
	Network based that are enabled in TCP packets
	Embed in the image itself
	Invisible watermarks such as yellow dots on printers

Other Types
	Audio 
	Video

Tokenization
	Replace sensitive data with a non-sensitive placeholder
	-SSN 226-12-1112 is now 691-61-8539
	Common with credit card processing 
	Uses a temporary token during payment and an attacker capturing the card number can't use them later
	Not encrypting or hashing as the original data or token aren't mathematically related
	![[Professor Messer - Obfuscation - CompTIA Security+ SY0-701 - 1.4 [LfuTMzZke4g - 942x530 - 6m29s].png]]

Data masking 
	Data obfuscation hides some of the original data
	Protects PII and other sensitive data
	May be hidden from view while the data still be intact in storage and control the view based on permissions
	Many different techniques such as substituting, shuffling, encrypting, masking out, etc

# Hashing and Digital Signatures

Hashes
	data as a short sting of text
	impossible to recover the original message from the digest and used to store passwords/confidentiality 

Example 
	SHA256 hash 256 bits

Collision
	Hash functions take an input of any size, create a fixed size string, message digest, checksum
	Hash should be unique, different inputs should never create the same hash, if they do it's a collision
	MD5 has a collision problem and isn't used anymore

Practical Hashing
	Verify a downloaded file, hashes may be provided on the download site and compare the downloaded file hash with the posted hash value
	password storage, instead of storing the password, store a salted hash, compare hashes during the authentication process, nobody ever knows your actual password

Adding some salt
	salt is random data added to a password during hashing
	every user gets their own random salt and the salt is commonly stored with the password
	rainbow tables won't work with salted hashes and additional random value added to the original password
	slows things down for brute forcing

Digital Signature
	prove the message was not changed for integrity
	proves the source of the message
	makes sure the signature isn't fake
	sign with the private key and verify with the private key

# Blockchain Technology

Blockchain
	A distributed ledger can keep track of transactions
	everyone on the blockchain network maintains the ledger and records and replicates to anyone and everyone
	Many practical applications such as payment processing digital identification, supply chain monitoring, and digital voting

# Certificates

Digital certificate
	a public key certificate that binds a public key with a digital signature
	a digital signature adds trust PKI uses certificate authorities for additional trust
	Web of trust adds other users for additional trust
	Certificate creation can be built into the OS and is part of windows domain services

Root of Trust
	everything associated with IT security requires trust as a foundational characteristic
	third party trusts sites as a foundation called
	The Root of Trust

Certificate Authorities 
	Allows trust for websites
	CA has digitally signed the website certificate
	if you can trust the CA, then you can trust the website

Third-party certificate authorities 
	Built-in to your browser
	can purchase your website certificate and can be trusted by everyone's browser
	CA is responsible for vetting the request

Certificate signing requests
	create key pair, then send the public key to the CA to be signed 
	The CA validates the request and confirms DNS emails and website ownership
	CA digitally signs the cert and returns to the applicant

Private Certificate Authorities 
	You are your own CA and you build it in house
	Needed for medium-to-large organizations and many web servers and privacy requirements
	Implement as part of your overall computing strategy

Self-signed certificates
	Internal certificates don't need to be signed by a public CA as your company is the only one that is going to use it
	No need to purchase trust devices that already trust you
	Build your own CA and issue your own certificates signed by your own CA 
	install the CA certificate/trusted chain on all devices, and they'll now trust any certificates signed by your internal CA

Wildcard Certificates
	Subject Alternative name (SAN)
	Lists additional identification information 
	Allows a certificate to support many different domains 
	Wildcard domain certificates are based on the name of the server

Key revocation
	Certificate revocation list (CRL)
	maintained by the CA and can contain many revocations in a large file
	Many different reasons to revoke CA's 

OSCP stapling
	online certificate status protocol provides scalability for OSCP checks
	The CA is responsible for responding to all client OSCP request and does not scale well
	Instead, have the certificate holder verify their own status and status information is stored on the certificate holder's server

Getting revocation details to the browser
	OSCP (Online Certificate Protocol) can have the browser check certificate revocation
	Messages usually sent to an OSCP responder via HTTP are easy to support over internet links and are more efficient than downloading a CRL
	Not all browsers/apps support OSCP as early Internet Explorer versions do not
	Some support, some don't, don't bother checking


# Take https://www.examcompass.com/comptia-security-plus-practice-test-2-exam-sy0-701 and https://www.examcompass.com/comptia-security-plus-practice-test-5-exam-sy0-701 to practice these concepts

And take chapter 1 of David Seidl - CompTIA Security+ Practice Tests_ Exam SY0-701-Sybex (2024) to practice concepts more