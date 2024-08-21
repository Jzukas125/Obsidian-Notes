In depth look at Nmap

# Intro
Nmap is an important network reconnaissance tool that is used to map out networks, hence the name. It does so by scanning ports to establish a parameter of running devices, It can fully map out devices using ports because each device creates its own port when its connected to the internet. Ports are necessary for making multiple network requests or having multiple services available. It helps by redirecting traffic to its approximate places.

Network connections are made between two ports, an open port and a randomly selected port on your own device. Every computer has a total of 65535 available ports; however, many of these are registered as standard ports. 

It is crucial we perform a scan on networks to find any open ports and with Nmap being our tool of choice. 

# Overview
When port scanning Nmap, there are three basic scan types. These are:
- TCP connect scans (-sT)
- SYN "Half-open" scans (-sS)
- UDP Scans (-su)

Additionally there are several less common port scan types, some of which we will also cover. These are:
- TCP null scans (-sN)
- TCP FIN scans (-sF)
- TCP Xmas Scans (-sX)