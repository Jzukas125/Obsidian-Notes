#TryHackMe 
# Intro
NetworkMiner is an open-source traffic sniffer, pcap handler, and protocol analyzer. Developed and maintained by Netresec. Usually described as a network forensic analysis tool or a NFAT for windows. It is expected that basic Linux and network fundamentals are known. 

Network forensics is a specific subdomain of the forensics domain but it focuses on network traffic investigation. The investigation process attempts to discover what is called the 5W: Who (Source IP and port), What (Data/payload), Where (Destination IP and port), When(Time and data), and Why (How/What happened).

# What is NetworkMiner
In a nutshell:
	Traffic Sniffing - It can intercept the traffic, sniff it, and collect and log packets that pass through the network 
	Parsing PCAP files - Parse pcap files and show the content of the packets in detail 
	Protocol analysis - Can identify the used protocols from the parsed pcap files
	OS fingerprinting - Can identity the used OS by reading the pcap file. Strongly relies on Satori and p0f
	File extraction - Can extract images, HTML files and emails from the parsed pcap file
	Credential grabbing - Can extract credentials from the parsed pcap file
	Clear text keyword parsing - Can extract cleartext keywords and strings from the parsed pcap file 

It has two operating modes:
	Sniffer mode: Available only on windows, not as reliable as other features, don't use as a primary sniffer. 
	Packet Parsing/Processing: NetworkMiner can parse traffic captures to have a quick overview and information capture. This operation mode is mainly suggested to grab the "low hanging fruit" before diving into a deeper investigation

Pros and Cons 
Pros: 
- OS fingerprinting 
- Easy file extraction 
- Credential grabbing 
- Clear test keyword parsing 
- Overall overview 
Cons:
- Not useful in active sniffing
- Not useful for large pcap investigation
- Limited filtering 
- Not built for manual traffic investigation 

# Tool Overview 1

Landing Page
	Home page of the application

File Menu 
	File menu helps load a pcap file or receive pcap over IP. Can also drag and drop pcap files as well. NetworkMiner also can receive pcaps over IP. 

Tools Menu
	Tool menu helps clear the dashboard and remove the captured data

Help Menu
	Provides information on updates and the current version

Case Panel 
	Shows the lit of the investigated pcap files. You can reload/refresh, view metadata details and remove loaded files from this panel.

Hosts
	Hosts menu shows the identified hosts in the pcap file. This section provides information on;
	- IP address
	- MAC Address 
	- OS type 
	- Open ports 
	- Sent/Received packets
	- Incoming/Outgoing sessions
	- Host details 
OS fingerprinting uses the satori GitHub repo and p0f, and the MAC address database uses the mac-ages GitHub repo. 

Sessions
	The session menu shows detected sessions in the pcap file. The section provides information on; Frame number, Client and server address, Source and destination port, protocol, and start time.
	Can search for keywords inside frames with the help of the filtering bar. It is possible to filter specific columns of the session menu as well. This menu accepts four types of input; "ExactPhrase", "AllWords", "AnyWord", "RegExe". 

DNS
	The DNS menu shows DNS queries with details. This section provides information on;
	- Frame number
	- Timestamp
	- Client and server
	- Source and destination port
	- IP TTL
	- DNS time
	- Transaction ID and type
	- DNS query and answer
	- Alexa Top 1M

Credentials
	Credentials menu shows extracted credentials and password hashes from investigated pcaps. Can use Hashcat and John the Ripper to decrypt extracted credentials. NetworkMiner can extract credentials including;
		- Kerberos hashes
		- NTLM hashes
		- RDP cookies
		- HTTP cookies
		- HTTP requests
		- IMAP 
		- FTP 
		- SMTP
		- MS SQL

Files
	file menu shows extracted files from investigated pcaps. This section provides information on;
	- Frame number
	- Filename
	- Extension
	- Size
	- Source and destination address
	- Source and destination port
	- Protocol 
	- Timestamp 
	- Reconstructed path 
	- Details 

Images
	file menu shows extracted images from investigated pcaps. The right-click menu is helpful in this part as well. 

Parameters
	File menu shows extracted parameters from investigated pcaps. This section provides information on;
	- Parameter name 
	- Parameter value 
	- Frame number
	- Source and destination host
	- Source and destination port
	- Timestamp
	- Details

Keywords
	The file menu shows extracted keywords from investigated pcaps. Section provide information on;
	- Frame number 
	- Timestamp
	- Keyword
	- Context
	- Source and Destination host
	- Source and destination port

Messages
	The messages menu shows extracted emails, chats, and messages from investigated pcaps. This section provides information on;
	- Frame number
	- Source and destination host
	- Protocol
	- Sender (From)
	- Receiver (To)
	- Timestamp
	- Size

Anomalies
	The anomalies menu shows detected anomalies in the processed pcap. Note that NetworkMiner isn't designated as an IDS. However, developers added some detections for EternalBlue exploit and spoofing attempts.

# Version Differences
The most significant differences between version 1.6 and 2.7 are as follows:

Mac Address Processing
	workMiner after version 2 can process MAC address specific correlation. This option will help identify if there is a MAC address conflict. 

Sent/Received Packet Processing 
	workMiner versions up to version 1.6 can handle packets in much detail. These options will help you investigate the sent/received kets in a more detailed format. This feature is not available 

Frame Processing 
	Any version after 1.6 cant handle frames 

Parameter Processing
	NetworkMiner version after version 2 can handle parameters in a more extensive form. 

Cleartext Processing
	NetworkMiner versions up to version 1.6 can handle cleartext data. This option provides all extracted cleartext data in a single tab; it is beneficial to investigate cleartext data about the traffic data. However, it is impossible to match the cleartext data and packets.

Remember that this tool is usually used for a brief look at packets and should not be a main sniffer. 