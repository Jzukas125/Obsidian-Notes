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
