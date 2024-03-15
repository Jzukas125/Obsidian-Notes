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
	Network Intrusion Prevention System (NIPS) - Monitors the traffic flow from various areas of the network. The aim is to protect the traffic on the entire subnet.
	Behavior-based Intrusion Prevention System (Network Based Analysis - NBA) -Monitors the traffic flow from various areas of the network. Aims to protect the traffic on the entire subnet. If a signature is identified, the connection is terminated. Requires a training period in order to function well.
	Wireless Intrusion Prevention System (WIPS) - Monitors the traffic flow from a wireless network. Aims to protect wireless traffic and stop possible attacks that could be launched from there. If a signature is identified, the connection is terminated.