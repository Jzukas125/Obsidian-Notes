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
Logs will be covered later on. Zeek automatically begins traffic investigation or on a pcap or generating logs automatically. Once a pcap is processed with Zeek, it will create logs in the working directory. If Zeek is run as a service, logs will be located in the default log path. The default log path for Zeek is /opt/zeek/logs

<h3> Working with Zeek </h3>
There are two operation options for Zeek, The first one is running it as a service, and the second option is running against zeek against pcap. Before starting working with zeek, let's check the version of the Zeek Instance with the following command: zeek -v which checks zeek's version

The ZeekControl module requires super permissions to use. You can elevate the session privileges and switch to the super user account to examine the generated log files with the following commands: sudo 

Here we can manage the Zeek service and view the status of the service. Primary management of the Zeek service is done with three commands; "status", "start", and "stop".

You can use the "ZeekControl" mode with the following commands as well;
- zeekctl status
- zeekctl start
- zeekctl stop

The only way to listen to the live network traffic is using Zeek as a service. Apart from using the Zeek's as a network monitoring tool, we can also use it as a packet investigator. To do so, we need to process the pcap files with Zeek, as shown below. Once you process a pcap file, Zeek automatically creates log files according to the traffic.

In pcap processing mode, logs are saved in the working directory. You can view the generated logs using the ls- l command. 

- Main Zeek command line parameters are as follows:
	- -r : reading option
	- -C: ignoring checksum errors
	- -v: version info
	- zeekctl: ZeekControl module

# Zeek Logs

Zeek generates log files according to the traffic data. You will have logs for every connection in the wire, including the application level protocols and fields. Zeek is capable of identifying 50+ logs and categorizing them into seven categories. Zeek logs are well structured and tab-separated ASCII files, so reading and processing them is easy but requires effort. You should be familiar with networking and protocols to correlate the logs in an investigation, know where to focus, and find a specific piece of evidence 

Each log output consists of multiple fields, and each field holds a different part of the traffic data. Correlation is done through a unique value called UID. The UID represents the unique identifier assigned to each session.

Basic of Zeek Logs:
- Category - Description - Log Files
- Files - File analysis result logs - files.log, oscp.log, pe.log, x509.log
- NetControl - Network control and flow logs - netcontrol.log, netcontrol_drop.log, netcontrol_shunt.log, netcontrol_catch_relase.log, openflow.log
- Detection - Detection and possible indicator logs - intel.log, notice.log, notice_alarm.log, signatures.log, traceroute.log
- Network Observations - Network flow logs - known_certs.log, known_hosts.log, known_modbus.log, known_services.log, software.log
- Miscellaneous - Additional logs cover external alerts, inputs and failures - barnyard2.log, dpd.log, unified2.log, unknown_protocols.log, weird.log, weird_stats.log
- Zeek diagnostic - Zeek diagnostic logs cover system messages, actions and some statistics - broker.log, capture_loss.log, cluster.log, config.log, loaded_scripts.log, packet_filter.log, print.log, prof.log, reporter.log, stats.log, stderr.log, stdout.log

Some log files are updated daily, and some are updated in each session. Some of the most commonly used logs are explianed as so:
- **Daily Logs:**
  - `known_hosts.log`: List of hosts that completed TCP handshakes.
  - `known_services.log`: List of services used by hosts.
  - `known_certs.log`: List of SSL certificates.
  - `software.log`: List of software used on the network.
- **Per Session Logs:**
  - `notice.log`: Anomalies detected by Zeek.
  - `intel.log`: Traffic contains malicious patterns/indicators.
  - `signatures.log`: List of triggered signatures.

A difficulty that occurs when working with Zeek is having the required network knowledge and investigation mindset. Luckily these are attainable through continuing cybersecurity concepts and activities.

Brief log usage primer table:
- Overall Info - Protocol Based - Detection - Observation
- conn.log - http.log - notice.log - known_host.log
- files.log - dns.log - signatures.log - known_services.log
- intel.log - ftp.log - pe.log - software.log
- loaded_scripts.log - ssh.log - traceroute.log - weird.log

Logs can be categorized before starting an investigation. Thus, finding the evidence/anomaly you are looking for will be easier. The given table is a brief example of using multiple log files. You can create your working model or customize the given one. Make sure you read each log description and understand the purpose to know what to expect from the corresponding log file. Note that these are not the only ones to focus on. Investigated logs are highly associated with the investigation case type and hypothesis, so do not just rely on the logs listed.

List Explained:
- Overall Info - The aim is to review the overall connections, shared files, loaded scripts and indicators at once. This is the first step of investigations
- Protocol Based - Once overall traffic is reviewed and suspicious indicators are found or you want to conduct a more in-depth investigations, you focus on specific protocol.
- Detection - Use the prebuild or custom scripts and signature outcomes to support your findings by having additional indicators or linked actions
- Observations - the summary of the hosts, services, software, and unexpected activity statistics will help you discover possible missing points and conclude the investigation<br> 
Remember, we mention the procs and cons of the Zeek logs at the start of the task. Now let's demonstrate the log viewing and identify the differences between them.
- Recall 1: Zeek logs are well structured and tab-separated ASCII files, so reading and processing them is easy but requires effort 
- Recall 2: Investigating the generated logs will require command-line tools and additional tools<br> 
In addition to Linux command-line tools, one auxiliary program called zeek-cut reduces the effort of extracting specific columns from log files. Each log files provides "filed names" in the beginning. This information will help you while using zeek-cut. Make sure that you use the "fileds" and not the "types". 

Let's see the "zeek-cut" in action. Let's extract the uid, protocol, source and destination hosts, and source and destination ports from the conn.log. We will first read the logs with the cat command and then extract the event of interest fields with zeek-cut auxiliary to compare the difference. 

# CLI Kung-Fu Recall: Processing Zeek Logs

GUIs are handy and good for accomplishing tasks and processing information quickly. There are multiple advantages of GUIs, especially when processing the information visually. HOWVER, when processing massive amounts of data, GUIs are not stable and as effective as the CLI tools.<br> 
The critical point is: What if there is no "function/button/feature" for what you want to find/view/extract.
<br>   Having the power to manipulate the data at the command line is a crucial skill for ananlysts. Not only in this room but each time you deal with packets, you will need to use command-line tools, Berkley Packet Filters (BPF) and regular experssions to find/view/extract the data you are looking for. This task provides quick cheat-sheet like information to help you write CLI queries for your event of interest.
<br> I will try to translate the table into note form

![[Pasted image 20240402144702.png]]
- Use Case : Description
- Sort | uniq : Remove duplicate values
- sort | uniq -c : Remove duplicates and count the number of occurrences for each value 
- sort -nf : Sort values numerically and recursively 
- rev : REverse string chracters
- cut -f 1 : Cut field 1
- cut -d '.' -f 1-2 : Split the sting on every dot an print keeps the first two fields
- grep -v 'test' : Display lines that don't match the "test" sting
- grep -v -e 'test1' -e 'test2' : Display lines that don't match one or both "test1" and "test2" strings
- file : view file information 
- grep -rin Testvalue1 * | column -t | less -S : Search the "Testvalue1" string everywhere, organize column spaces and view the output with less

# Zeek Signatures
