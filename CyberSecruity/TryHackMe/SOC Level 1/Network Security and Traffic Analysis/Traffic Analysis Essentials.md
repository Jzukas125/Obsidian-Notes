#TryHackMe 
# Introduction

Network Security is a set of operations for protecting data, applications, devices, and systems connected to the network. It focuses on the system design, operation, and management of the architecture/infrastructure to provide network accessibility, integrity, continuity, and reliability. This is important to know because traffic analysis is a subdomain of the network security domain, and its primary focus is investigating the network data to identify problems and anomalies.

# Network Security and Network Data

Base Network Security Control Levels:
	Physical: Physical controls prevent unauthorized physical access to networking devices, cable boards, L components.
	Technical: Data security controls prevent unauthorized access to network data, like installing tunnels and implementing 
	Administrative: Administrative security controls provide consistency in security operations like creating policies, assess levels, and authentication processes 

The main approaches:
	Access Control: Starting point of network security
	Threat Control: Detecting and preventing anomalous/malicious activity

Key elements of Access Controls:
	Firewall Protection - Controls Incoming and outgoing network traffic with predetermined security rules
	NAC (network access controls) - Controls the devices' suitability before access to the network, verifies device specifications
	IAM (identity and access management) - Controls and manages the asset identities and user access to data systems and resources 
	Load Balancing - Controls the resource usage to distribute tasks over a set of resources over the and improve overall data processing flow
	Network Segmentation - Creates and controls encrypted communication between devices 
	VPN - Creates and controls encrypted communication between devices
	Zero trust model - suggests configuring and implementing the access and permissions at a minimum level

Key elements of Threat Control:
	IDS/IPS - Inspects the traffic and creates alerts (IDS) or resets the connection (IPS) when detecting an anomaly 
	DLP (Data Loss Prevention) - Inspects the traffic and blocks the extraction of sensitive data 
	Endpoint Protection - Protecting all kinds of endpoints and appliances that connect to the network by using a multi-layered approach like encryption, antivirus, antimalware, DLP, and IDS/IPS
	Cloud Security - Protecting cloud/online-based systems resources from threats and data leakage by applying suitable countermeasures 
	SIEM - Technology that helps threat detection, compliance, and security incident management.
	SOAR (Security Orchestration Automation and Response) - Technology that helps coordinate and automates tasks between various people, tools, and data
	Network Traffic Analysis & Network Detection and Response - Inspecting network traffic or traffic capture to identify anomalies and threats 

Typical Network Security Management Operation is in four categories: 
Deployment 
	Device and software installation
	Initial configuration 
Configuration
	Feature configuration
	Initial network access configuration
Management 
	Security policy implementation
	NAT and VPN implementation
	Threat mitigation
Monitoring
	System monitoring
	User activity monitoring
	Threat monitoring
	Log and traffic sample capturing 

# Managed Security Services

Network Pentesting
	Assessing network security by simulating external/internal attacker techniques to breach the network
Vulnerability Assessment
	Assessing network security by discovering and analyzing vulnerabilities in the environment
Incident Response 
	An organized approach to addressing and managing a security breach. It contains a set of actions to identify, contain, and eliminate incidents.
Behavioral Analysis 
	An organized approach to addressing system and user behaviors, creating baselines and traffic profiles for specific patterns to detect anomalies, threats, vulnerabilities, and attacks.

# Traffic Analysis / Network Traffic Analysis

Traffic analysis - a method of intercepting, recording/monitoring, and analyzing network data and communication patterns to detect and respond to system health issues, network anomalies, and threats.

Two main techniques in traffic analysis:
Flow Analysis 
	Collecting data/evidence from the networking devices. This type of analysis aims to provide statistical results through the data summary without applying in-depth packet level investigation. Easy to collect and analyze but it does not provide full packet details
Packet Analysis
	Collecting all available network data. Applying in-depth pack-level investigation to detect and block anomalous and malicious packets. Provides full packet details but requires higher skills and more time



