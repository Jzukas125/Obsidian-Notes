
# Take this for an acronym test 

// will add in later

# Threat Actor

Threat Actors
	Entity responsible for an event that has an impact on the safety of another entity is called a malicious actor
	Threat actor attributes describes characteristics of the attacker
	Useful to categorize the motivation 

Attributes
	Internal/external could be inside or outside the company
	Resources/funding 
	Level of sophistication/capability can determine if they blindly run scripts or have automated vulnerability scans 

Motivations
	What is the purpose
	Motivations include, Data exfiltration, espionage, service disruption, blackmail, financial gain, philosophical, ethical, revenge, disruption, war

Nation states
	external entity which could be a government and national security
	many possible motivations such as data exfiltration, philosophical, revenge, disruption, war 
	constant attacks, massive resources, commonly an Advanced Persistent Threat
	Highest Sophistication usually have military control, utilities, and financial control
	US used Stuxnet worm on Israel

Unskilled attackers
	runs pre-made scripts without any knowledge of what's really happening
	motivated by the hunt 
	can be internal or external
	not very sophisticated 
	no formal funding 

Hacktivist
	Hacker with a purpose can be motivated by philosophy revenge, disruption, etc.
	often an external entity
	Can be remarkably sophisticated and have very specific hacks 

Insider Threat
	Motivated by revenge or financial gain 
	Extensive resources that use the organization's resources against themselves
	Medium level of sophistication 

Organized Crime
	professional criminals that are motivated by money 
	Very sophisticated  
	Crime that's organized with one person hacking, one person managing the exploits, another person selling the data, and another handling customer support
	Lots of capital to fund hacking

Shadow IT
	Working around the internal IT organization and builds their own infrastructure 
	IT can put up roadblocks, they are unencumbered, use the cloud, and might be able to innovate
	Limited resources and have a company budget
	Medium sophistication and may not have IT training or knowledge

# Threat Vector 

Threat Vector
	method used by an attacker to gain access or infect the target
	a lot of work goes into finding vulnerabilities in these vectors as some may be more vulnerable than others
	IT security professionals spend their career watching these vectors protect existing vectors and find new vectors 

Message Based Vectors
	One of the biggest threat vectors
	Email could have malicious links or links to a malicious site
	SMS could have attacks in a text message

Message-based vectors
	phishing attacks 
	could deliver the malware to the user such as attaching it to an email
	Social engineering scams

Image based vectors
	easy to identify a text based threat
	Some image formats can be a threat such as SVG or XML
	Significant security concerns like an HTML injection or JavaScript attack code
	Browsers must provide input validation and should avoid running malicious code

File based vectors
	more than just executables and can have malicious code hide in many places
	adobe PDF is a file format containing other objects 
	ZIP/RAR files could contain many different files
	Microsoft Office could have documents with macros and add-in files 

Voice call Vectors 
	Vishing - phishing over the phone 
	Spam over the IP - large scale phone calls 
	War dialing - trying to find unpublished phone numbers to gain access to systems
	Call tampering - disrupting voice calls

Removable device vectors
	get around the firewall with a USB interface
	malicious software on USB flash drives can infect air gapped networks like industrial systems, and high-security services
	USB (universal serial bus) devices can act as keyboards 
	Data exfiltration can have terabytes of data walk out the door and use zero bandwidth

Vulnerable software vectors
	Client based that can have infected executables, known vulnerabilities, and may require constant updates
	Agentless has no installed executables, compromised software on the server that would affect all the users 

Unsupported systems vectors
	patching is an important prevention tool that has ongoing security fixes
	unsupported systems aren't patched and may not be
	outdated operating systems 
	single system could be an entry that keeps your inventory and records current

Unsecured network vectors
	network connects everything
	wireless may have outdated security protocols with open or rogue wireless networks 
	Wired also has unsecure interfaces - No 802.1x 
	Bluetooth has implementation vulnerabilities

Open service ports
	Most network based services connect a TCP or EDP port
	Every open port is an opportunity for the attacker application vulnerability or misconfiguration 
	Every application has their own port and more services expand their attack surface
	Firewall rules must allow traffic to an open port

Default Credentials 
	Most devices have default usernames and passwords 
	The right credentials provide full control 
	Very easy to find the defaults for your access point or router

Supply chain vectors
	tamper with the underlying infrastructure or manufacturing process
	Managed service providers(MSPs)  access many different customer networks from one location
	Gain access to a network using a vendor such as the 2013 target credit card breach
	Suppliers include counterfeit networking equipment that install backdoors, substandard performance and availability an incident includes 2020 fake Cisco catalyst switches

# Phishing

Phishing 
	Social engineering with a touch of spoofing that is usually delivered by email or text and is very remarkable when well done
	Can be proven wrong by checking the URL
	Usually something's not quite right such as spelling, fonts, or graphics

Business email compromise
	We trust email sources then attackers take advantage of this trust
	Spoofed email addresses are not legitimate email addresses
	Financial fraud sends emails with bank information and modify wire transfer details 

Tricks and misdirection
	digital sleight of hand 
	typosquatting which is a type of URL hijacking
	pretexting has lying to get info with the attacker being in character in a situation they create

Phishing with different bait
	Vishing is done over the phone or voicemail with caller ID spoofing is common
	Smishing (SMS phishing) is done by text message, spoofing is a problem here as well and forwards links or asks for personal information
	Variations on a theme such as the fake check scam, phone verification code scam, Boss/CEO scam, advance-fee scam

# Impersonation

Pretext
	before the attack the trap is set with an actor and a story

Impersonation
	attackers pretend to be someone they aren't
	use some of those details from reconnaissance 
	attacking the victim as someone higher in rank 
	throw tons of technical details around 
	be a buddy

Eliciting Information
	extracting information from the victim
	often seen with vishing and can be easier to get this info over the phone
	Well-documented psychological techniques

Identity fraud 
	identity can be used by others 
	Credit card fraud will have them open an account in your name or use your credit card information
	Bank fraud will have an attacker gain access to your account or open a new account
	Loan fraud is used for a loan or lease 
	Government benefits fraud where attacks obtain benefits on your behalf

Protect against impersonation
	newer volunteer information
	don't disclose personal details
	always verify before revealing info 
	verification should be encouraged 

# Watering Hole

Watering hole attack
	attack that infects websites they typically visit and lure them to a malicious site
	attackers can't get in 
	Have the mountain come to you, go to where the mountain hangs out, the watering hole

Executing the watering hole attack
	determine which website the victim group uses
	Infect one of these third-party sites 
	infect all visitors

Watching the watering hole attack 
	Defense in depth such as layered defense 
	Firewalls and IPS stops the network traffic before things get bad
	Anti-virus/Anti-malware signature updates

# Other Social Engineering Attacks

Misinformation/disinformation
	disseminate factually incorrect information can create confusion and division
	Influence campaigns can sway public opinion on political and social issues
	Nation-state actors can divide, distract, and persuade
	Advertising is an option
	Enabled through social media 

The misinformation process
![[Pasted image 20240126101852.png]]

Brand impersonation
	Pretend to be a well-known brand
	Create tens of thousands of impersonated sites which you can do in google index, click an ad, get a WhatsApp message
	Visitors are presented with a pop-up
	Malware infection is almost guaranteed

# Take https://www.examcompass.com/comptia-security-plus-practice-test-6-exam-sy0-701 to practice the before mentioned concepts 
# Memory Injections

Finding Malware
	malware runs in memory and memory forensics can find the malicious code
	memory contains running processes such as DLLs, threads, buffers, memory management functions and much more
	malware runs its own process and injects itself into a legitimate process 

Memory Injection
	add code into memory of an existing process that hides malware inside of the process
	get access to the data in the process and the same rights and permissions and perform a privilege escalation

DLL injection
	Dynamic-Link Library (DLL)
	A windows' library containing code and data and many applications can use this library
	Attackers inject a path to a malicious DLL runs as part of the target process
	One of the most popular memory injection methods are relatively easy to implement 

# Buffer Overflows

Buffer overflows
	overflowing, a buffer of memory spills over into other memory areas
	developers need to perform bounds checking the attackers spend a lot of time looking for openings
	not a simple exploit and takes time to avoid crashing things and to make it do what you want it to do
	A really useful buffer overflow is repeatable which means that a system can be compromised 

# Race conditions

Race condition
	a programming conundrum with some things happening at the same time and this can be bad if you're not planned for it 
	time to check to time of use attack (TOCTOU), check the system, when do you use the results of your last check?, something might happen between the check and the use

Race Conditions can cause big problems
	January 2004 - Mars rover "Spirit"
	Reboot when a problem is identified
	Problem is with the file system, so reboot because of the file system problem
	Reboot loop was the result

# Malicious Updates

Software Updates
	always keep your OS and applications updated, and most updates have bug fixes and security patches 
	the process has its own security concerns
	follow best practices always have known-good backups 
	install from a trusted source 

Downloading and updating 
	install updates from a downloaded file, always consider your actions, every installation could potentially could be malicious 
	confirm the source, a random pop-up during web browsing may not be legitimate
	visit the developer's site directly, don't trust a random update button or random downloaded file
	many operating systems will only allow signed apps, do not disable your security controls

Automatic Updates 
	app updates itself and often include security checks / digital signatures
	Relatively trustworthy and comes directly from the developer
	SolarWinds Orion supply chain attack was reported in December 2020, attackers gained access to the SolarWinds development system

# Operating System Vulnerabilities

Operating Systems 
	foundational computing platform, as everyone has an OS which makes it a big target
	Remarkably complex with millions of lines of code
	Vulnerabilities are there, we just haven't found them yet

A month of OS updates
	normal month of Windows updates is a patch every 2nd Tuesday

Best practices for OS vulnerabilities
	Always update monthly or on-demand updates 
	May require testing before deployment
	May require a reboot, make sure to save all data

# SQL injection

Code injection 
	code injection is adding your own information into a data stream
	enabled because of bad programming and where the application should properly handle input and output
	So many different data types such as HTML, SQL, XML, LDAP, etc.

SQL injection
	SQL is structured Query language and is the most common relational database management system language
	SQL (SQLi), put your own SQL requests into an existing application
	Can often be executed in a web browser with it being in a form or a field

Building a SQL injection
	Could view all database info, delete datebase information, add users, etc

# Cross-site scripting

Cross-site scripting
	XSS 
	originally called cross-site because of browser security flaws
	One of the most common web app vulnerabilities as it takes advantage of the trust a user has for a site 
	XSS commonly uses JavaScript

Non-persistent XSS attack
	Website allows scripts to run in user input
	Attack emails a link that takes advantage of this vulnerability
	Script embedded in URL executes in the victim's browser
	Attacker uses credentials/session IDs/cookies to steal a victim's information with their knowledge

Persistent XSS attack
	attacker posts a message to a social network
	it is now persistent 
	No specific target - goes for everyone
	For social networking this can spread very quickly

Hacking a Subaru
	June 2017, Aaron Guzman 
	When authenticating with Subaru users get a token that never expires
	Valid token allowed any service request even adding your email address to someone's account, and now you have full access 
	Web front-end included an XSS vulnerability and if a user clinks a malicious link you now have their token

Protecting against XSS
	Be careful when clicking untrusted links, never blindly click your email inbox
	Consider disabling JavaScript or control with an extension
	Keep your browser and applications updated 
	Validate input 

# Hardware Vulnerabilities

Hardware vulnerabilities
	Surrounded by hardware devices, many of which do have an accessibly operating system
	These devices are potential security issues
	Always update firmware
	IoT is everywhere
	Security landscape has grown

Firmware
	software inside of hardware which is the Os of the device
	vendors are the only one can fix their hardware assuming they know about the problem
	Trane comfortlink II thermostats - trans notified of 3 vulnerabilities took several years to patch

End-of-Life
	End of life (EOL) manufacturer stops selling, and supporting the product
	End of Service life (EOSL) manufacturer stops selling a product and support is no longer available for the product
	Technology EOSL is a significant concern

Legacy Platforms
	Some devices remain installed for a long time 
	Legacy devices have older operating systems, applications, or middleware
	May be running end-of-life software and the risk needs to be compared to the return
	May require additional security protections

# Virtualization Vulnerabilities

Virtualization Security
	Quite different from a non-virtual machines
	Quantity of resources vary between VMs such as CPU, memory, and storage
	Many similarities to physical machines, complexity adds opportunity for the attackers

VM escape protection
	Virtual machine is elf-contained, or is it?
	Virtual machine escape can break out of the VM and interact with the host operating system or hardware
	Once you escape the VM, you have great control over the host and other guest VMs
	this would be a huge exploit and give you access to full control of the virtual world

Escaping the VM
	March2017 - Pwn2Own competition hacking contest
	JavaScript engine bug in Microsoft Edge with code executing in the edge sandbox
	Windows 10 kernel bug compromised the guest operating system
	Hardware simulation bug in VMware 

Resource Reuse
	hypervisor manages the relationship between physical and virtual resources
	These resources can be reused between VMs, hypervisor host with 4gb of ram and supports VMs with 2Gb of ram each, ram is allocated and shared between VMs

# Cloud Specific vulnerabilities

Security in the cloud
	cloud adoption has been nearly universal, and it is difficult to find a company not using the cloud 
	Put lots of sensitive data in the cloud 
	We are not putting in the right protections, 76% of organizations aren't using MFA for management console users
	Simple best practices aren't being used 63% of code in production is unpatched 
	Vulnerabilities rated high or critical

Attack the service 
	Denial of Service (DoS)
	Authentication bypass can take advantage of weak or faulty authentication
	Directory traversal faulty configurations put disk at risk 
	Remote code execution can also take advantage of unpatched systems

Attack the application
	Web application attacks have increased, such as log4j
	Cross-site scripting (XSS) take advantage of poor input validation
	Out of bounds write unauthorized memory areas such as data corruption, crashing, or code execution
	SQL injection can get direct access to a database

# Supply chain vulnerabilities 

Supply chain risk
	chain contains many moving parts such as raw materials, suppliers, manufacturers, distributors, customers, consumers
	Attackers can infect any step along the way and can infect different parts of the chain without suspicion and people trust their suppliers
	One exploit can infect the entire chain, meaning there is a lot at stake

Service Providers
	you can control your own security posture and can't always control a service provider
	service providers often have access to internal services 
	many different types of providers such as network, utility, office cleaning, payroll/accounting cloud services, system admin
	Consider ongoing security audits of all providers

Example
	40 million credit cards were stolen 
	Heating and AC firm has an email with malware sent to it
	HVAC vendor was the supplier and had access to the same network as the cash registers

Hardware providers
	Can you trust your new server/router/switch/firewall which is the supply chain cybersecurity	
	Use a small supplier base
	Strict controls over policies and procedures ensure proper security is in place
	Security should be part of the overall design and there's a limit to trust

Cisco or not Cisco
	all network traffic flows through switched and routers which a perfect visibility and pivot point
	Knock-offs made in China and sold as authentic

Software Providers
	trust is a foundation of security and every software installation questions our trust 
	 initial installation have digital signature should be confirmed during installation 
	 Updates and patches, some software updates are automatic 
	 Open source is not immune and compromising the source code itself

SolarWinds Supply chain attack
	SolarWinds Orion was used by 18000 customers
	Software updates compromised in March and June 2020 and upgrades to existing installations
	not detected until December 2020
	Additional breaches took advantage of the exploit

# Misconfiguration Vulnerabilities 

Open permissions 
	very easy to leave a door open and the hackers will always find it
	increasingly common with cloud storage

Unsecured admin accounts
	Linux root account, windows admin, or superuser
	can be a misconfiguration intentionally configuring an easy-to-hack password
	disable direct login to the root account by using the su or sudo option
	Protect accounts with root or administrator access 

Insecure protocols 
	Some protocols aren't encrypted, and all traffic sent in the clear
	Verify with a packet capture and can view everything sent over a network
	Use the encrypted versions such as SSH, SFTP, IMAPS, etc

Default Settings
	every application and network device has a default login and not all of these are ever changed
	Mirai botnet takes advantage of default configurations and takes over IoT devices with 60+ default configurations
	Mirai released as open source software

Open ports and services
	Services will open ports and is important to manage access
	often managed with a firewall manages traffic flows and will allow or dent based on port number or application 
	Firewall rulesets can be complex 

# Mobile Device Vulnerabilities

Mobile Device security
	challenging to secure and often needs additional security policies and systems
	relatively small can be almost invisible 
	almost always in motion and will never know where it might be
	packed with sensitive data and personal and organizational data
	Constantly connected to the internet 

Jailbreaking/rooting
	mobile devices are purpose-built systems and you don't have to access to the operating system
	Gaining access, android with rooting and apple with jailbreaking
	Uncontrolled access can circumvent security features and MDM (mobile device management) becomes relatively useless

Sideloading
	malicious apps can be a significant security concern 
	manage installation apps 
	Sideloading circumvents security and apps can be installed manually without using an app store making your MDM useless

# Zero Day Vulnerabilities 

Vulnerabilities 
	many applications have vulnerabilities and we just haven't found them
	someone is working had to find the next big one
	attackers keep these yet-to-be-discovered holes to themselves and they want to use these vulnerabilities to their personal gain

Zero-day attacks
	attackers search for unknown exploits and create exploits against these vulnerabilities 
	The vendor has no idea it even exists and don't have a fix for it
	zero-day attacks is an attack without a patch or method of mitigation 
	a race to exploit the vulnerability or create a patch

# Overview of Malware

Malware
	Malicious software can be bad
	gather information keystrokes
	show you advertising
	viruses and worms

Malware types and methods
	Viruses, Worms, Ransomware, Trojan Horse, Rootkit, Keylogger, Spyware, Bloatware, Logic Bomb

How you get it 
	These all work together
	A worm takes advantage of a vulnerability and installs malware that includes a remote access backdoor and additional malware may be installed later
	Your computer must run a program such as email links, web page pop-ups, drive-by download, worm
	Your computer is vulnerable, always update your OS

Your data is valuable
	Personal data such as family pictures or important documents
	Organization data such as, planning documents, employee personally, Employee personally identifiable information (PII), financial information, and company private data

Ransomware
	a particularly nasty malware 
	Malware encrypts your data files 
	Must pay the attackers to obtain the decryption key 

Protecting against ransomware
	always have an offline backup
	keep your operating system up to date
	keep your applications up to date
	keep your anti-virus/anti-malware signatures up to date 
	keep everything updated

# Viruses and Worms

Virus 
	Malware that can reproduce itself and it needs you to execute a program
	Reproduces through file system or the network and can spread from just running a program can spread a virus 
	May or may not cause problems 
	Anti-virus is very common and there are thousands of new viruses every week
	Anti-virus goes through computer and scans for commonly know malicious files

Virus Types
	program viruses are a part of the application
	Boot sector viruses 
	Script Viruses
	Macro viruses

Fileless virus
	a stealth attack that does a good job of avoiding anti-virus detection
	Operates in memory but is never installed in a file or application

![[Pasted image 20240128110145.png]]

Worms 
	malware that self-replicates and doesn't need you to do anything
	Uses the network as a transmission medium
	Self-propagates and spreads quickly
	worms can take over systems pretty quickly

Wannacry worm
	self propagated and installed ransomware

# Spyware and Bloatware

Spyware
	malware that spies on you, such as advertising, identity theft, or affiliate fraud
	Can trick you into installing
	Browser monitoring
	Keyloggers

Protecting against spyware
	maintain your anti-virus
	always know what you're installing 
	Where's your backup?
	can use malware bytes to run scams for your system

Bloatware
	new computer of phone includes the OS and important apps
	also includes apps you didn't expect and don't need
	apps are installed by the manufacturer 
	uses valuable storage space and may also add to overall resource usage and the system may be slower than expected

Removing bloatware
	identify and remove
	use the built-in uninstaller
	some apps have their own uninstaller
	third party uninstallers and cleaners

# Other malware types

Keyloggers
	your keystrokes contain valuable information such as web site login URLs, passwords, email messages
	Saves all of your input and sends it to bad actors
	Circumvents encryption protections
	Other data logging such as clipboard logging, screen logging, instant messaging, and search engine queries

Logic bomb
	waits for a predefined event and often left by someone with a grudge
	Time bomb with a time or date
	User event logic bomb
	Difficult to identify and difficult to recover 

Preventing a logic bomb
	difficult to recognize as each is unique 
	process and procedures with formal change control
	electronic monitoring such as alert changes 
	constant auditing an administrator can circumvent exiting systems

Rootkit
	originally a Unix technique
	modifies core system files and is part of the kernel
	can be invisible to the operating system 
	also invisible to traditional anti-virus utilities

Finding and removing rootkits
	look for the unusual anti-malware scans 
	use a remover specific to the rootkit
	secure boot with UEFI with security in the BIOS

# Physical attacks

Physical attacks
	old-school security
	many different ways to circumvent digital security and a physical approach must be considered
	if you have physical access to a server, you have full control, and an OS can't stop an in-person attack
	Door locks keep out the honest people

Brute Force
	the physical version 
	push through the obstruction
	check your physical security

RFID cloning
	RFID is everywhere
	duplicators are on amazon and are less than $50 and takes less than a second
	this is why we have MFA

Environmental attacks
	attack everything supporting the technology 
	power monitoring
	HVAC and humidity controls 
	Fire suppression

# Denial of Service 

Denial of service
	force a service to fail by overloading the service
	take advantage of a design failure or vulnerability 
	cause a system to be unavailable 
	create a smokescreen for some other exploit
	doesn't have to be complicated such as turning the power off

A friendly Dos
	unintentional DoSing
	network DoS layer 2 loop without STP
	Bandwidth DoS downloading multi-gigabyte Linux distro over a DSL line
	the water line breaks

DDoS 
	Launch an army of computers to bring down a service
	This is why the attackers have botnets thousands or millions of computers at your command
	At its peak, Zeus botnet infected over 3.6 million PCs
	Asymmetric threat and the attacker may have fewer resources than the victim

DDoS reflection and amplification 
	Turn your small attack into a big attack and is often reflected off another device or service
	An increasingly common network DDoS technique
	Uses protocols with little (if any) authentication or checks such as NTP, DNS, ICMP and is a common example of protocol abuse

# DNS Attack

DNS poisoning
	modify the DNS server and requires some crafty hacking
	modify the client host file and the host file takes a precedent over DNS queries
	send a fake response to a valid DNS request and requires a redirection of the original request or the resulting response
	Real-time redirection
	This is an on-path attack

Domain Hijacking
	get access to the domain registration, and you have control where the traffic flows, and you don't need to touch the actual servers and determines the DNS names and DNS IP addresses
	many ways to get into the account such as brute forcing, social engineering the password, and gaining access to the email address that manages the account

URL Hijacking
	make money from your mistake and there's a lot of advertising on the net
	spell the badly spelled domain to the actual owner
	redirect to a competitor
	phishing site

Types of URL hijacking
	typosquatting/brandjacking - taking advantage of poor spelling
	outright misspelling - professormesser.com vs. professormessor.com
	A typing error - professormeser.com
	different phrase - professormessers.com
	different top-level domain - professormesser.org

# Wireless Attacks

802.11 management frames
	802.11 wireless includes a number a management features
	frames that make everything work
	Important for the operation of 802.11 wireless, how to find access points manage QoS, associate/disassociate with an access point, etc
	Original wireless standards did not add protection for management frames

Protecting against deauth attacks
	IEEE has already addressed the problem 
	Some of the important management frames are encrypted
	Not everything is encrypted

Radio frequency (RF) jamming
	denial of service that prevents wireless communication
	transmit interfering wireless signals by decreasing the signal to noise ratio at the receiving device 
	Sometimes it's not intentional
	Jamming is intentional

Wireless jamming
	many different types like constant, random bits/Constant, legitimate frames
	Data sent at random times
	Reactive jamming
	Needs to be somewhere else difficult to be effective from a distance
	Fox hunting is used for hunting down the jammer 

# On-path attacks

On-path network attack
	man in the middle attack
	redirects your traffic and then passes it on to the destination
	never know your traffic was redirected
	ARP poisoning, on-path attack on the local IP subnet, works because ARP has no security

On-path browser attack
	Man in the browser attack does malware/trojan and does all of the proxy work
	Huge advantages for the attackers and is relatively easy to proxy encrypted traffic and everything looks normal to the victim
	the malware in your browser waits for you to login to your bank

# Replay attacks

Replay attacks
	useful information is transmitted over the network and a crafty hacker will take advantage of this
	need access to the raw network data, can be obtained with a network tap or ARP poisoning
	the gathered information may help the attacker
	This is not an on-path attack and the actual replay doesn't require the original workstation

Pass the hash
	form of replay attack
	starts with client sending authentication request to the computer 
	Attacker then sends his own authentication request and then gets a hashed password and username which still allow logging in
	Avoid this type of replay attack by using encryption and using salting 

Browser cookies and session IDs
	cookies are information stored on your computer
	used for tracking, personalization, and session management 
	could be considered to be a privacy risk
	session IDs are often stored in the cookie

Header manipulation
	could be gathered using Wireshark
	could modify headers using tamper or firesheep
	modify cookies such as cookies manager
	many sites are not HTTPS only

Prevent session hijacking
	encrypt end-to-end, can't capture session ID if they can't see it 
	Additional load on the web server
	encrypt end-to-somewhere, at least avoid capture over a local wireless network

# Malicious Code

Exploiting a vulnerability
	an attacker can use many techniques such as social engineering or such
	don't require much technical skills
	still ways to get into a well-secured system

Malicious Code
	attackers can use any opportunity and the types of malicious code are varied
	many different forms 
	protection comes from many different sources such as anti-malware, firewall, continuous updates and patches

Malicious code examples
	Wannacry ransomware 
	British Airways XSS used 22 lines of malicious JavaScript code placed on checkout pages and had info stolen from 380,000 victims 
	Estonian central health database had an SQL injection that breached all healthcare information for an entire country

# Application attacks

Injection attacks
	Code injection - adding your own info into a data stream
	enabled because of bad programming and the application should properly handle input and output
	Many different injectable data types such as HTML, and SQL

Buffer Overflows
	spills into other memory areas
	not a simple exploit and it takes time to avoid crashing things
	a really useful buffer overflow is repeatable which means that system can be compromised

Privilege Escalation
	gain higher level access to a system by exploiting a vulnerability and might be a bug or design flaw
	Higher level access means more capabilities
	high-priority vulnerability patches 
	Horizontal privilege escalation as user A can access user B resources

Mitigating privilege escalation 
	patch quickly and fix the vulnerability
	updated anti-virus to block known vulnerabilities
	data execution prevention

Cross-site requests 
	cross-site requests are common and legitimate
	HTML on a website directs requests from your browser 

The client and the server
	website pages consist of client-side code and server-side code
	client side renders the page on the screen
	Server side performs requests from the client such as transferring money from one account to another

Cross-site request forgery
	one-click attack, session riding
	takes advantage of the trust that a web application has for the user, the web site trusts your browser, and requests are made without your consent or your knowledge
	Significant web application development oversight 

![[Pasted image 20240129192712.png]]

Directory traversal
	directory traversal/path traversal that reads files from a web server that are outside of the website's file directory, users shouldn't be able to browser the Windows folder
	Web server software vulnerability won't stop users from browsing past the web server root
	Web application code vulnerability can take advantage of badly written code

# Cryptographic Attacks

Cryptographic Attacks
	the attacker doesn't have the combination so they break the safe 

Birthday Attack
	in a classroom of 23 students what is the chance of two students sharing a birthday, about 50%
	In the digital world this is hash collision, a hash collision is the same hash value for two different plaintexts
	the attacker will generate multiple versions of plaintext to match the hashes, protect yourself with large hash output size

Collisions 
	hash digests are supposed to be unique and different input data should not create the same hash
	md5 is the message digest algorithm 5 with collisions identified in 1996

Downgrade attack
	instead of using a perfectly good encryption use something that's not so great and force the systems to downgrade their security
	SSL stripping combines an on-path attack with a downgrade attack, difficult to implement, but big returns for the attacker, attacker must sit in the middle of the conversation, victims browser page isn't encrypted and strips the S from HTTPS

# Password Attacks 

Plaintext/unencrypted passwords
	some applications store passwords in the clear with no encryption
	do no store passwords as plaintext or anyone with access to the password file or database has every credential

Hashing a password 
	hashes represent data as a fixed-length string of text 
	Impossible to recover the original message from the digest which makes it a common way to store passwords
	SHA-256 hash is a good example of a hash function

Spraying attack
	try to login with an incorrect password until you're locked out
	Attack an account with the top 3 passwords and if it doesn't work move to the next account

Brute force 
	try every possible combination until the hash is matched 
	brute force attacks online keep trying the login process, very slow, and most accounts will lockout after a number of failed attempts
	brute force offline - obtain the list of users and hashes, calculate a password hash, compare it to a stored hash, very large computational resource requirement 

# Indicators of compromise 

Indicators of compromise (IOC)
	an even that indicates an intrusion 
	Indicators are unusual amount of network activity, change to file hash values, changes to DNS data, uncommon login patterns, spikes of read requests to certain files

Account lockout
	credentials are not working
	exceeded login attempts
	account was disabled by admins
	may be part of a larger plan

Concurrent session usage
	challenging to be two places at one time 
	multiple account logins from multiple locations
	can be difficult to track down such as multiple devices or automated processes

Blocked content
	an attacker wants to stay as long as possible 
	Probably a security patch available 
	blocked content such as auto-update connections, links to security patches, third party anti malware sites

Impossible travel
	authentication logs can be telling 
	login from Omaha, Nebraska, United States
	3 minutes later, a login from Melbourne, Victoria, Australia
	Should be easy to identify 

Resource Consumption 
	every attacker's action has an equal and opposite reaction 
	file transfers use bandwidth an unusual spike at 3 am
	firewall logs show the outgoing transfer
	often the first real notification of an issue 

Resource inaccessibility
	server is down and not responding 
	network disruption and is a cover for the actual exploit
	server outage is the result of an exploit gone wrong
	encrypted data is potential of ransomware attack beginning

Out of cycle Logging
	Out-of-cycle occurs at an unexpected time
	operating system patch logs occurring outside of the normal patch day
	firewall log activity with timestamps of every traffic flow and protocols and applications used

Missing logs 
	log information is evidence and attackers will try to cover their tracks by removing logs
	information is everywhere such as authentication logs, file access logs, proxy logs, server logs
	logs may be incriminating as missing logs are certainly suspicious 

Published/Documented 
	entire attack and data exfiltration may go unnoticed
	company data may be published online and the attackers post a portion or all data
	raw data may be released without context 

# Segmentation and Access control 

Segmenting the network
	physical, logical, or virtual segmentation
	performance 
	Security such as users should not talk directly to database servers
	compliance, mandated segmentation

Access control lists
	allow or disallow traffic
	Restrict access to network devices can limit IP address or other identifier and prevent regular user / non admin access
	Be careful when configuring these
	list the permissions bob can read files, fred can access the network, james can access network 192.168.1.0
	Many operating systems use ACLs to provide access to files

Application allow list / deny list
	Any application can be dangerous 
	Security policy can control app execution 
	Allow list doesn't let anything run unless its approved
	Deny list doesn't let anything on its list run

Examples of allow and deny lists
	decisions are made in the operating system and are often built-in to the operating system management
	Application hash only allows applications with this unique identifier
	Certificate allows digitally signed apps from certain publishers
	Path only runs applications in these folders
	Network zone is the apps can only run from this network zone

# Mitigation Techniques

Patching 
	allows for system stability and security fixes
	monthly updates provides incremental and important
	third party updates such as application developers and device drivers
	auto update not always the best option

Encryption 
	prevent access to application data files
	file level encryption
	full disk encryption, encrypts everything on the drive 
	Application data encryption is managed by the app and stored data is protected

Monitoring
	Aggregate information from devices are built-in sensors, separate devices such as built-in sensors, separate devices that are integrated into servers, switches, routers, firewalls, and etc
	Sensors are intrusion prevention systems, firewall logs, authentication logs, web server access logs, database transaction logs, email logs
	Collectors monitor proprietary consoles, SIEM consoles, syslog servers and many SIEMs include a correlation engine to compare diverse sensor data

Least privilege
	rights and permissions should be set to the bare minimum
	All user accounts must be limited 
	Don't allow users to run with administrative privileges 

Configuration enforcement
	perform a posture assessment each time a device connects
	extensive check like OS patch version, EDR version, status of firewall and EDR, certificate status
	Systems out of compliance are quarantined like private VLAN with limited access and recheck after making corrections

Decommissioning
	should be a formal policy
	Mostly associated with storage devices 
	Many options for physical devices such as recycling the device for us in another system

# Hardening Techniques

System hardening
	many and varied for windows, Linux, iOS, Android
	Updates operating system updates/service packs, security patches
	User accounts like minimum password lengths and complexity and account limitations
	Network access and security could be limiting networking access

Encryption 
	prevent access to application data files with something like Windows Encrypting File System (EFS)
	Full disk encryption (FDE) encrypts everything
	encrypt all network communication

The endpoint 
	the user's access such as applications and data
	stop the attackers inbound and outbound attacks
	many different platforms
	protection is multi-faceted with defense being in depth

Endpoint detection and response
	a different method of threat protection should scale to meet the increasing the number of threats
	Detect a threat, signatures aren't the only detection tool
	Investigate the threat and find the root cause analysis
	Respond to the threat and isolate the system, quarantine the threat, rollback to a previous config API driven, no user or technician intervention required

Host based firewall
	software based firewall, personal firewall and runs on every endpoint
	allow or disallow incoming or outgoing application traffic can be controlled by the application process to view all data
	identify and block the unknown processes and stop malware before it can start
	Manage centrally

Finding Intrusions
	host based intrusion prevention system (HIPS) can recognize and block known attacks, Secure OS and application configs, validate incoming service requests and often built into endpoint protection software
	HIPS identification are signatures, heuristics, behavioral and buffer overflows, registry updates, writing files to the Windows folder and access to non-encrypted data

Open ports and services
	every open port is a possible entry point and you should close everything except required ports
	Control access with a firewall with NGFW being ideal
	Unused or unknown services installed with the OS or from other applications
	Applications with broad port ranges open port 0 through 65,535
	Use Nmap or similar port scanner to verify, ongoing monitoring is important

Default password changes
	every network device has a management interface with critical systems and other devices
	many applications also have management or maintenance interfaces and they can contain sensitive data
	change default settings like passwords
	add additional security that require logon and add 3rd party authentication

Removal of unnecessary software
	All software contains bugs and some of these bugs are security vulnerabilities
	Every application seems to have a completely different patching process and can be challenging to manage ongoing updates
	Remove all unused software to reduce you're risk and is an easy fix





