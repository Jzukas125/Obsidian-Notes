# Introduction
Zeek is an open-source and commercial network monitoring tool (traffic analyzer). "Many operators use Zeek as a network security monitor (NSM) to support suspicious or malicious activity investigations. Zeek also supports a wide range of traffic analysis tasks beyond the security domain, including performance measurement and troubleshooting." From the Official description 

Pre-requisites: Basic Linux knowledge and network fundamentals. 

# Network Security Monitoring and Zeek

Network security monitoring has been said many time in my notes and I am not retyping that. 

<h3> Zeek vs Snort </h3>
While both are IDS/NIDs, it is good to know the pros and cons of each tool and use them in a specific manner. While there are some overlapping functionalities, they have different purposes for usage. 

Capabilities
	Zeek
		NSM and IDS framework. It is heavily focused on network analysis. It is more focused on specific threats to trigger alerts. The detection mechanism is focused on events
	Snort
		An IDS/IPS system. It is heavily focused on signatures to detect vulnerabilities. The detection mechanism is focused on signature patterns and packets.

Pros
	Zeek
		Provides in-depth traffic visibility. Useful for threat hunting. Ability to detect complex threats. Has a scripting language and supports event correlation. Easy to read logs 
	Snort
		Easy to write rules. Cisco supported rules. Community support.

Cons
	Zeek
		The analysis is done out of the Zeek, manually or by automation
	Snort
		Hard to detect complex threats

Common Use Case
	Zeek
		Network monitoring. In-depth traffic investigation. Intrusion detecting in chained events.
	Snort 
		Intrusion detection and prevention. Stop known attacks/threats. 

<h3> Zeek Architecture </h3>
Zeek has two primary layers; "Event Engine" and "Policy Script Interpreter". The event engine layer is where the packets are processed; it is called the event core and is responsible for describing the even without focusing on event details. It is where the packages are divided into parts such as source and destination addresses, protocol identification, session analysis and file extraction. The policy script interpreter layer is where the semantic analysis is conducted. It is responsible for describing the event correlations by using Zeek scripts.
![[Pasted image 20240320142951.png]]

<h3> Zeek Frameworks </h3>
Available Frameworks include Logging, Notice, Input, Configuration, Intelligence, Cluster, Broker Communication, Supervisor, Geolocation, File Analysis, Signature, Summary, Decontrol, Packet Analysis, TLS Decryption. 

<h3> Zeek Outputs </h3>
Zeek provides 50+ log files under seven different categories, which are helpful in various areas such as traffic monitoring, intrusion detection, threat hunting, and web analytics. 
Logs will be covered later on. Zeek automatically begins traffic investigation or on a pcap or generating logs automatically. Once a pcap is processed with Zeek, it will create logs in the working directory. If zeek is run as a service, logs will be located in the default log path. The default log path for Zeek is /opt/zeek/logs
