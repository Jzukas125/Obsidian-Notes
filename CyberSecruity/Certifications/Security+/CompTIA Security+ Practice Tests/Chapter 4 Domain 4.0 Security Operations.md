#Securityplus
# 1-10
1. ~~B~~
2. ~~C~~
3. A
4. ~~A~~
5. ~~D~~
6. B
7. A
8. B
9. B
10. A
6/10

1 A is correct
John wants to harden his organization’s routers. If there are no currently known vulnerabilities or issues with the device, which of the following hardening options will provide the biggest benefit?
A. Moving their administrative interfaces to a protected VLAN
B. Disabling unnecessary services
C. Installing the most current patch level for the OS
D. Enabling SNMP-based logging

Moving to a vlan will provide the most significant improvement in security since there are no known issues or vulnerabilities at the moment. If there were, patching or disabling services would quickly move up.

2 B is correct
Jackson is reviewing his organization’s logs and discovers multiple new user accounts created after business hours using administrative credentials. What term describes searching for
potential issues like this?
A. IoC creation
B. Threat hunting
C. Root cause analysis
D. Eradication

Threat hunting is the process of searching for threats, often using IoCs. Root cause analysis looks for the underlying cause of an issue or event, and eradication is the complete removal of a threat or artifacts of malicious activity.

4 C is correct
Greg wants to gain admission to a network which is protected by a network access control
(NAC) system that recognized the hardware address of systems. How can he bypass this
protection?
A. Spoof a legitimate IP address.
B. Conduct a denial-of-service attack against the NAC system.
C. Use MAC cloning to clone a legitimate MAC address.
D. None of the above.

Greg can clone a mac address. Greg can do this by checking for a MAC label on some devices or by capturing traffic on the network if he can physically access it.

5 B is correct
Melissa’s organization has deployed a firewall that uses three interfaces to provide services.
The first interface connects to the Internet, the second to a network where the organization’s
web servers reside, and the third to a secured network where the organization’s workstations
are connected. What type of firewall architecture has Melissa’s organization deployed?
A. An ACL
B. A screened subnet
C. A binary firewall
D. A multihomed, multiroute NGFW

A screened subnet designs use a firewall with three interfaces, one for the internet or an untrusted network, one for a protected but front-facing network, and for one for a shielded or protected network. ACL (access control list) use rules to control access. NGFW can be multihomed but not multirouted.

# 11-20
11. C
12. C
13. ~~D~~
14. C
15. C
16. D
17. ~~D~~
18. ~~B~~
19. C
20. C
7/10

13 B is correct
Angela reviews bulletins and advisories to determine what threats her organization is likely
to face. What type of activity is this associated with?
A. Incident response
B. Threat hunting
C. Penetration testing
D. Vulnerability scanning

Threat hunting can also include reviewing advisories and bulletins to remain aware of the threat environment. Vulnerability scanning seeks to identify vulnerabilities using testing through technical means like connecting to services or checking local version information.

17 C is correct
Carolyn runs a vulnerability scan of a network device and discovers that the device is
running services on TCP ports 22 and 443. What services has she most likely discovered?
A. Telnet and a web server
B. FTP and a Windows file share
C. SSH and a web server
D. SSH and a Windows file share

A network device running SSH on port 22 and a web server on TCP port 443 is a very typical discovery when running a vulnerability scan. Without any demonstrated issues, Carolyn should simply note that she saw those services. Telnet runs on port 21, an unencrypted web server will run on TCP 80 in most cases, and Windows file shares use a variety of ports, including TCP ports 135–139 and 445.

18 C is correct
Susan is responsible for application development in her company. She wants to have all web
applications tested before they are deployed live. She wants to use a test system that is identical to the live server. What is this called?
A. A production server
B. A development server
C. A test server
D. A predeployment server

A test server should be identical to the production server. This can be used