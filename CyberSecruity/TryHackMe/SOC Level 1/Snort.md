# Intro
Pre-requisites: Should be familiar with basic Linux and network fundamentals. Network fundamentals is basically a requirement.
Snort - Open-sourced, rule0based NIDS/NIPS. 

# Interactive Material and VM
In the tryhackme environment it has an interactive vm that allows people to get hands on experience in snort.

# Introduction to IDS/IPS
A recap of what an IDS and IPS is needed before continuing. 

<h3> IDS (Intrustion Detection System) </h3>
IDS is a passive monitoring solution for detecting possible malicious activities/patterns, abnormal incidents, and policy violations. It is responsible for generating alerts for each suspicious event.
Two main Types of IDS are:
	Network Intrusion Detection System (NIDS) - Monitors the traffic flow from various areas of the network. It aims to investigate the traffic on the entire subnet. If a signature is identified, an alert is created.
	Host-based Intrusion Detection Systems (HIDS) - HIDs monitors the traffic flow from a single endpoint device. It aims to investigate the traffic on a particular device. If a signature is identified, an alert is created.

<h3> Intrustion Prvention System (IPS) </h3>
IPS is an active protecting solution for preventing possible malicious activities/patterns, abnormal incidents, and policy violations. It is responsible for stopping/preventing/terminating the suspicious event as soon as the detection is preformed. 
Four main types are as follows:
	- Network Intrusion Prevention System (NIPS) - Monitors the traffic flow from various areas of the network. The aim is to protect the traffic on the entire subnet.
	- Behavior-based Intrusion Prevention System (Network Based Analysis - NBA) -Monitors the traffic flow from various areas of the network. Aims to protect the traffic on the entire subnet. If a signature is identified, the connection is terminated. Requires a training period in order to function well that is also known as baselining.
	- Wireless Intrusion Prevention System (WIPS) - Monitors the traffic flow from a wireless network. Aims to protect wireless traffic and stop possible attacks that could be launched from there. If a signature is identified, the connection is terminated.
	- Host-Based Intrusion Prevention System (HIPS) - Protects the traffic flow from a single endpoint device. Aims to investigate the traffic on a particular device. If a signature is identified, the connection is terminated. Similar to HIDS but stops threats instead of alerting.

<h3> Detection Prevention Techniques </h3>
Three main detection techniques:
- Signature-Based - Relies on rules that identify the specific patterns of the known malicious behavior. Also detects known threats
- Behavior-Based - Identifies new threats with new patterns that pass through signatures. Compares the known/normal with unknown/abnormal behaviors. Detects previously unknown or new threats.
- Policy-Based - Compares detected activities with system configuration and security policies. This model helps detect policy violations.

Snort Overview 
Capabilities of Snort;  
- Live traffic analysis
- Attack and probe detection
- Packet logging
- Protocol analysis
- Real-time alerting
- Modules & plugins
- Pre-processors
- Cross-platform support! (Linux & Windows)

Snort has three main use models;  
- Sniffer Mode - Read IP packets and prompt them in the console application.
- Packet Logger Mode - Log all IP packets (inbound and outbound) that visit the network.
- NIDS (Network Intrusion Detection System)  and NIPS (Network Intrusion Prevention System) Modes - Log/drop the packets that are deemed as malicious according to the user-defined rules.

# My first Snort

Verify snort is installed with 
	snort -V

As a first step we should verify that our configuration file is valid by typing
```Shell
sudo snort -c /etc/snort/snort.conf -T
```
-T is for testing configuration
-c is identifying the configuration file (snort.conf) 

Once a configuration file is used, snort gains more power. The config file is an all-in-one management file of the snort. Rules, plugins, detection mechanisms, default actions and output settings are identified here. It is possible to have multiple configuration files for different purposes and cases but can only use one at run time. You can prevent the banned by using the -q parameter if you so need.

Some important parameters are as follows:
```shell
-V/- Provides snorts verison and information
-c Identififying the configuration file 
-T Snorts self-test parameter, you can test your setup with this parameter
-q Setups Quiet mode
```

# Sniffing Mode

Sniffer mode parameters are as follows:
```
-v Verbose, Displays TCP/IP output in the console
-d Displays the packet data
-e Display the link-layer
-X Display the full pakcet details in HEX
-i this parameter helps to define ap specifc network interface to listen/sniff. Once you have multiple interfaces, you can choose a specifc interface to sniff
```

# Logger Mode

Snort packet logging parameters:
```shell
-l Logger mode, target log and alert output directory. Default output folder is /var/log/snort. The default action is to dump as tcpdump format in /var/log/snort
-K ASCII Log packets in ASCII format
-r reading option, read the dumped logs in snort
-n specify the number of packets that will process/read. Snort will stop after reading the specified number
```

# IDS/IPS

Helps manage traffic according to user-defined rules
Parameters for IDS/IPS mode:
```
-c Defining the configuration file
-T testing hte configuration file
-N disable logging
-D background mode
-A Alert modes of which include, full(all alerts with full information), fast(shows alert, timestamp, source, and destination IP, along with port numbers), console(fast alerts on the console screen), cmg(cmg style basic headers), none(dissables alerts)
```

# PCAP Investigation

PCAP parameters are as follows:
```
-r/-pcap-single Read s ingle pcap file
-pcap-list="" Read pcaps provided in command
-pcap-show Show pcap name on console during processing
```

# Snort Rule Structure

![[Pasted image 20240316165142.png]]

Each rule represents a type of actions, protocol, source, and destination IP, source and destination port and an option. Remember, Snort is in passive mode by default meaning snort is usually an IDS. You will need to put it in inline mode to turn on IPS mode. 

Rules are easy to understand but difficult to produce.
Action rules:
	There are several actions for rules. Understanding the functionality and testing it before creating rules for live systems. The most common actions are listed below. 
	Alerts - generate an alert and log the packet
	Logs - log the packet
	Drop - Block the log and packet
	Reject - Block the packet, log it, and terminate the packet session
Protocol rules:
	Protocol parameter identifies the type of protocol that filtered for the rule.
	Snort2 supports only four protocols filters in the rules. However, you can detect the application flows using port numbers and options. 

<h3>  IP and Port Numbers </h3>
Parameters to identify the source and destination IP addresses and associated port numbers filtered for the rule:
IP Filtering - alert icmp 192.168.1.56 <> any any  This rule will create an alert for each ICMP packet originating from the 192.168.1.56 IP address
Filter an IP range - alert icmp 102.168.1.0/24 any <> any any  This rule will  create an alert for each ICMP packet originating from the 192.168.1.0/24 subnet
Filter multiple IP ranges - alert icmp [192.168.1.0/24, 10.1.1.0/24] any <> any any   This rule will create an alert for each ICMP packet originating from the 192.168.1.0/24 and 10.1.1.0/24 subnets.
Exclude IP addresses/ranges - alert icmp !192.168.1.0/24 any <> any any  This rule will create an alert for each ICMP packet not originating from the 192.168.1.0/24
Port filtering - alert tcp any any <> any 21  This rule will create an alert for each TCP packet sent to port 21
Exlcude a specifc port - alert tcp any any <> any !21  This rule will create an alert for each TCP packet not sent to port 21
Exclude a port range (Type 1)- alert tcp any any <> any 1:1024  This rule will create an alert for each TCP packet
Filter a port range (Type 2) - alert tcp any any <> any 1:1024  This rule will create an alert for each TCP packet sent to ports less than or equal to 1024
