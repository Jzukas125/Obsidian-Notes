Notes taken from meeting hosted by Dallas Desimone

# Types of Network Monitoring Tools
- Packet capture and analyzer: Capture Network Packets
- Firewall: Controls incoming and outgoing network traffic with predetermined security rules 
- IDS/IPS: Intrusion Detection and Intrusion Prevention Systems inspects the traffic and creates alerts or resets the connection when detecting an anomaly/threat 

- PCAP Analyzers
	- Wireshark
	- Zeek
	- Network Miner
	- Brim

- Firewalls
	- Palo Alto Networks: PA Series firewalls
	- Fortinet: FortiGate ser4ies firewalls
	- Cisco: Cisco Secure Firewall
	- Check Point: Check Point Quantum Security Gateway
	- Sophos: Sophos XG Firewall, Sophos UTM firewalls
- Free Firewalls
	- pfSense: FOSS hardware firewall software
	- OPNsense: FOSS hardware firewall software
	- Windows Firewall: Built into Windows 

# Types of IDPS/IPS

Types:
1. NIDS: Deployed at strategic points on your network, such as the firewall or core router.
2. HIDS: installed directly on individual devices, such as servers, desktops, and laptops.
Detection Methods:
1. Signature-Based Detection: Most common type of detection method
2. Anomaly-Based Detection: Anomaly-based IDS/IPS system monitor network traffic or system activity for unusual patterns. Helpful for zero-day detection
3. Policy-Based Detection: Compares detected activities with system configuration and security policies. 

# Snort
Good for writing rules to test them
