#Securityplus 
# 1-10
1. C
2. C
3. ~~D~~
4. ~~D~~
5. B
6. ~~C~~
7. ~~C~~
8. C
9. C
10. ~~D~~
5/10

3 B is correct
You are a security administrator for a medium-sized bank. You have discovered a piece of
software on your bank’s database server that is not supposed to be there. It appears that the software will begin deleting database files if a specific employee is terminated. What best
describes this?
A. Worm
B. Logic bomb
C. Trojan horse
D. Rootkit

A logic bomb is malware that performs malicious activity when some condition is met. A rootkit is malware with root privileges. Not specified if this malware has root access so it is not a rootkit.

4 C is correct
The company that Yarif works for uses a third-party IT support company to manage their
cloud-hosted web application infrastructure. How can Yarif best address concerns about
potential threat vectors via the managed service provider (MSP)?
A. Conduct regular vulnerability scans.
B. Use shared incident response exercises to prepare.
C. Ensure appropriate contractual coverage for issues.
D. Require the MSP to have an annual pentest.

Using appropriate contractual terms is usually the best available option for handling third-party vendor risk. The terms can include things like security practices, such as pentesting, incident response exercises, and vulnerability scanning, and can also have sufficient penalties to ensure ongoing compliance from responsible companies.

6 B is correct
Helen is concerned about ransomware attacks against workstations that she is responsible for. Which of the following hardening options is best suited to protecting her organization from ransomware?
A. Installing host-based firewalls
B. Installing endpoint protection software
C. Installing a host-based IPS software
D. Removing unnecessary software

Endpoint protection software like an endpoint detection and response (EDR) or extended detection and response (XDR) tool will provide the greatest protection against ransomware. Firewalls and IPS are less likely.

7 B is correct
The company that Gary works for has deployed a wireless network. Which of the following network options is the most secure?
A. WPA-2 Personal
B. WPA-3
C. WPA-2 Enterprise
D. WPA-4

WPA-3 is the most modern, most secure option from the list. WPA-4 does not exist and WPA-2 is less secure.

# 11-20
11. A
12. B
13. ~~A~~
14. ~~A~~
15. B
16. B
17. C
18. D
19. B
20. B
8/10

13 C is correct
Which of the following is not a common concern related to the hardware vendor
supply chain?
A. Malware preinstalled on hardware
B. Lack of availability of hardware
C. Third-party hardware modifications
D. Malicious firmware modifications

While malware, modified firmware, and a lack of availability are common concerns with the hardware supply chain, hardware modifications remain relatively uncommon.

14 B is correct
Ben wants to conduct a credential replay attack. What should he do first to enable
the attack?
A. Create a phishing email.
B. Conduct an on-path attack.
C. Use a brute-force password attack.
D. Conduct an injection attack.

On-path attacks are used to capture, then replay valid credentials for attackers to use. Phishing emails and brute forcing can help obtain credentials but do not involve credential replay.

# 21-30
21. A
22. ~~A~~
23. ~~A~~
24. ~~B~~
25. D
26. D
27. B
28. B
29. ~~C~~
30. B
6/10

22 C is correct
The organization that Mike works in finds that one of their domains is directing traffic
to a competitor’s website. When Mike checks, the domain information has been changed,
including the contact and other administrative details for the domain. If the domain had not
expired, what has most likely occurred?
A. DNS hijacking
B. An on-path attack
C. Domain hijacking
D. A zero-day attack

Domain hijacking or domain theft occurs when the registration or other information for the domain is changed without the original registrant's permission. DNs hijacking inserts false information into a DNS server.

23 C is correct
Lucia’s organization has adopted open source software provided by a third-party vendor
as part of their web application. What concern should she express about her software
supply chain?
A. Lack of vendor support
B. Lack of code auditability
C. Lack of control over open source dependencies
D. Lack of updates

Open source software dependencies are a primary challenge when considering open source supply chain concerns. In this case, Lucia is using a 3rd party vendor who can provide supports, open source code is auditable, and updates are likely to occur with a vendor involved.

24 A is correct
Alice wants to prevent server-side request forgery (SSRF) attacks. Which of the following will
not be helpful for preventing them?
A. Removing all SQL code from submitted HTTP queries
B. Blocking hostnames like 127.0.01 and localhost
C. Blocking sensitive URLs like /admin
D. Applying allow list–based input filters

Server side request forgery attempts typically to get HTTP data passed through and will not include SQL injection. Blocking sensitive hostnames, IP addresses, and URLs are all valid to prevent SSRF, as is the use of allow list-based input filters.

29 B is correct
Frank is a network administrator for a small college. He discovers that several machines
on his network are infected with malware. That malware is sending a flood of packets to a
target external to the network. What best describes this attack?
A. SYN flood
B. DDoS
C. Botnet
D. Backdoor

His machines are a part of a Ddos attack. This scenario describes a generic ddos attack. These machines could be part of a botnet or they may just have a trigger that causes them to launch the attack at a specific time. The real key in this scenario is the DDoS attack.

# 31-40
31. A
32. D
33. ~~C~~
34. ~~C~~
35. B
36. ~~B~~
37. ~~C~~
38. B
39. ~~A~~
40. A
5/10

33 A is correct
You have noticed that when in a crowded area, you sometimes get a stream of unwanted text messages. The messages end when you leave the area. What describes this attack?
A. Bluejacking
B. Bluesnarfing
C. Evil twin
D. Rogue access point

Bluejacking involves sending unsolicited messages to Bluetooth devices when they are in range. An evil twin uses a rogue access point whose name is similar or identical to that of a legitimate access point. Bluesnarfing is stealing data via Bluetooth.

34 A is correct
Dennis uses an on-path attack to cause a system to send traffic to his system and then forwards it to the actual server the traffic is intended for. What information will be visible from his system as it passed through it?
A. All traffic meant for remote systems
B. All traffic meant for local systems
C. Only unencrypted traffic
D. Only unencrypted traffic meant for his system

An on-path attack redirects all traffic through an attacker's system that would normally pass through a network gateway. Dennis will be able to see all traffic bound for remote systems, but some of it may be encrypted.

36 A is correct
Jake’s vulnerability scanner reports that the software his organization is running is vulnerable to a cryptographic downgrade attack. What concern should Jake have about this potential issue?
A. Attackers may be able to force use of a weaker encryption algorithm, making data easier
to access.
B. Attackers may be able to force use of weaker hashing, making it easier to recover
passwords.
C. Attackers may be able to force use of older versions of the software, including previously
patched vulnerabilities.
D. Attackers may be able to force encryption to be turned off, causing information to be
sent in plain text.

Cryptographic downgrade attacks like POODLE, FREAK, and Logjam all rely on flaws that cause software to use weaker encryption options. This could allow attackers to capture traffic encrypted with weaker encryption, potentially allowing them to decrypt the traffic and read it. They do not allow hashing changes to recover passwords, reversion to old versions of software, or encryption to be entirely turned off

37 D is correct
Rick has three major categories of data and applications in use in his virtualization environment: highly sensitive; business sensitive; and unclassified, or public information. He wants
to ensure that data and applications of different sensitivity are not compromised in the event
of a breach. What mitigation technique is best suited to this type of requirement?
A. Application allow lists
B. Monitoring
C. Least privilege
D. Segmentation

Segmentation can be used to separeate systems of different sensitivity. Least privilege is an effective practice to ensure only the rights required are in place, but does not meet the goal.

39 C is correct
As part of a zero-trust environment, Quentin is given rights that he needs only when he needs
them through a checkout process and they are then removed when he is done. What mitigation technique best describes this solution?
A. Segmentation
B. Isolation
C. Least privilege
D. Configuration enforcement

This is an example of least privilege implementation where only the privileges required are issued. Segmentation is used to separate systems or environments.

# 41-50
41. ~~D~~
42. ~~A~~
43. C
44. B
45. B
46. D
47. ~~C~~
48. C
49. A
50. B
7/10

# 51 - 60
51. ~~D~~
52. C
53. B
54. ~~D~~
55. ~~D~~
56. A
57. ~~C~~
58. ~~B~~
59. B
60. ~~D~~
4/10

51 B is correct
Renee has a large number of workstations and servers in her corporate environment and
wants to more effectively monitor logs for them. What solution from the following list is best
suited to identifying and alerting on issues in a large-scale environment?
A. Centralized logging
B. A SIEM
C. An IPS
D. An EDR

A SIEM is designed to ingest and analyze large volumes of logs and alerts. EDR's are not used for log management

54 C is correct
The following graphic shows a network connection between two systems, and then a
network-based attack. What type of attack is shown?
![[Pasted image 20240904122004.png]]
A. A denial-of-service attack
B. A SQL injection attack
C. An on-path attack
D. A directory traversal attack

An on-path attack redirects traffic to allow an attacker to see and potentially modify the traffic.  Directory traversal is just in browser manipulation.

55 D is correct
Which of the following protocols is most commonly associated with credential relaying
attacks?
A. RDP
B. NTLM
C. SQL
D. TLS

NTLM while dated is historically of the most common targets of credential relay attacks. RDP,SQL, and TLS are less commonly associated with credential relay attacks.

57 D is correct
Derek wants to conduct a birthday attack against a digital signature. Which of the following
best describes the process he would need to take to achieve his goal?
A. He needs to prepare both a correct and a malicious document and find ways to modify
the correct document until its encryption matches the malicious document.
B. He needs to make sure all dates match in both a correct and a malicious document.
C. He needs to ensure that the file length and creation date match for both a correct document and a malicious document.
D. He needs to prepare both a correct and a malicious document, then find ways to modify
the malicious document until its hash matches the hash of the correct document.

A birthday attack requires that hashes match for both an original document and a malicious document. He will modify the malicious document until he finds a way to convey the changes he needs while retaining the matching hash. This type of attack is why hashing algorithms needs to be resistant to birthday attacks.

58 A is correct
Ashley’s organization has recently come under attack and has suffered a DNS outage. As she investigated, she found that requests to her DNS servers were sent to open DNS resolvers using spoofed IP addresses with requests that would result in very large responses from the DNS resolvers to the IP addresses that appeared to be making the request. What type of attack targeted Ashley’s organization?
A. A reflected DDoS
B. A DNS flood
C. A mirrored DDoS
D. A supersized query attack

Ashley's company is victim to a reflected DDoS attack where attackers took advantage of DNS queries to make a small amounts off spoofed traffic into very large amounts of data sent to her servers.

60 C is correct
Kara wants to protect against the most common means of firmware-based exploits. Which of
the following is not a common firmware defense mechanism for the vendors of devices that
use firmware?
A. Using signed firmware updates
B. Using input validation for user input
C. Encrypting firmware
D. Code review processes for firmware

Firmware is typically not encrypted, but it is commonly digitally signed. Using input validation and code review both help to keep it secure.

# 61-70
61. ~~A~~
62. B
63. C
64. A
65. ~~A~~
66. ~~A~~
67. ~~D~~
68. C
69. ~~A~~
70. B
5/10

61 D is correct
Annie’s organization has been facing negative social media campaigns for months and is
struggling to address them. Numerous bot posts about the company are providing incorrect
information about the company. What type of attack is Annie’s company facing?
A. A misinformation campaign
B. A pretexting campaign
C. An impersonation campaign
D. A disinformation campaign

Annie's company is facing a disinformation campaign. If users were getting facts wrong than that would be misinformation, but since wrong information is being intentionally spread it is disinformation.

65 C is correct
Raj wants to reduce the attack surface for a newly purchased laptop. What hardening
technique will help him reduce the possibility of remote exploits while also decreasing the
amount of ongoing patch management he needs to do for the system?
A. Encrypt the system’s boot drive.
B. Install EDR software.
C. Remove unnecessary software.
D. Change any default passwords.

Removing unnecessary software reduces a system's attack surface and also means that he wont have to patch and maintain the software he removes. 

66 C is correct
Mary has discovered that a web application used by her company does not always handle
multithreading properly, particularly when multiple threads access the same variable. This
could allow an attacker who discovered this vulnerability to exploit it and crash the server.
What type of error has Mary discovered?
A. Buffer overflow
B. Logic bomb
C. Race conditions
D. Improper error handling

A race condition can occur when multiple threads in an application are using the same variable and the situation is not properly handled. A buffer overflow is putting more information into a buffer than it can handle.

67 C is correct
Allan wants to detect brute-force physical attacks. What should he do if he wants to detect
the broadest range of physical attacks?
A. Deploy a monitored security camera system.
B. Hire a guard to patrol the facility.
C. Conduct regular inspections of the facility.
D. Set up an alarm system

A monitored camera system will detect the broadest range of attacks. An alarm system won't detect attacks by insiders, who may access spaces they have access to in order to perform malicious attacks.

69 B is correct
During a regular review of logs, Jennifer notices that a regularly scheduled script that copies
files to another server every hour has run multiple times within the last hour. What indicator
of compromise should she categorize this as?
A. Concurrent session use
B. Out-of-cycle logging
C. Missing logs
D. Impossible travel

This is out of cycle logging. It could simply indicate a flaw in the script or another innocuous issue.

# 71-80
71. B
72. D
73. B
74. ~~C~~
75. B
76. ~~B~~
77. ~~C~~
78. ~~A~~
79. A
80. ~~A~~
5/10

74 A is correct
Dana wants to use documented and published IoCs as part of her threat-hunting activities.
What should she look for to integrate with her SIEM or other security tools?
A. Threat feeds
B. A real-time blackhole list
C. A vulnerability feed
D. An IP reputation feed

Both commercial and private threat feeds can be used by security tools like SIEM, EDR, and XDR systems to provide them with current information. 

76 D is correct
You are responsible for software testing at Acme Corporation. You want to check all software for bugs that might be used by an attacker to gain entrance into the software or your
network. You have discovered a web application that would allow a user to attempt to put a
64-bit value into a 4-byte integer variable. What is this type of flaw?
A. Memory overflow
B. Buffer overflow
C. Variable overflow
D. Integer overflow

Placing a larger integer into a smaller integer is integer overflow. Memory and variable overflow are not real terms.

77 A is correct
The company that Keith works for uses a backoff algorithm that increases the time between
when login attempts are allowed after each failed login. Keith has recently attempted to log
in and found that his account is not able to log in again for 15 minutes. What should the
security administrators at Keith’s organization do to find potential indicators of malicious
activity?
A. Review authentication logs.
B. Interview Keith about his recent logins.
C. Change Keith’s password and check error logs.
D. Report an incident and start the incident response process.

Until more is known the best route for security is to review the authentication logs in order to gather more information that can indicate whether an issue or security event has occurred. 

78 C is correct
Grayson’s organization is concerned about environmental attacks against their datacenter.
What type of monitoring is best suited to detecting environmental attacks in a scenario
like this?
A. Video cameras
B. Intrusion alarm systems
C. Temperature monitoring sensors
D. Log analysis

Environmental monitoring involves things like temperature, water or flood sensors, and other detection capabilities that help organizations know if a natural disaster or other environmental issue has occurred.

80 B is correct
Amanda is assessing the potential for issues with her organization’s recently adopted IaaS
vendor. What cloud vulnerability should she worry about if her system administrators do not
effectively manage security groups in AWS?
A. Insecure APIs
B. Misconfigurations
C. Malicious insiders
D. MFA-based attacks

Security groups are used like firewall rules in AWS and since Amanda's system administrators are not effectively managing security groups, this is most likely to create a misconfiguration. APIs are provided by the vendor and thus their security is typically a vendor issue.

# 81 - 90
81. ~~B~~
82. ~~B~~
83. C
84. ~~D~~
85. C
86. C
87. B
88. B
89. ~~A~~
90. ~~D~~
5/10

81 D is correct
Jared’s organization runs Linux servers, and recent vulnerability scans show that the servers
are vulnerable to an issue that is described as follows:
CVE-2018-5703: tcp_v6_syn_recv_sock function in net/ipv6/tcp_ipv6.c in
the Linux kernel through 4.14.11 allows attackers to cause a denial of
service (slab out-of-bounds write)
What is Jared’s best option to remediate a kernel vulnerability like this?
A. Patch the application.
B. Install a HIPS with appropriate rules.
C. Segment the systems away from the Internet to reduce risk.
D. Patch the operating system.

The Linux kernel is part of the operating system and needs to be handled with an OS patch. 

82 C is correct
it used the word encryption when the correct answer was hash

84 B is correct
What technique most effectively prevents resource reuse concerns for storage in a virtual
environment?
A. Firmware updates
B. Volume encryption
C. Minimizing cluster size
D. Reformatting drives

Ensuring that any volume that is used in a virtual environment is encrypted when created will prevent reuse concerns because data will be unrecoverable even if encrypted data was accessible. Firmware updates, cluster sizes, and reformatting do not properly address this issue.

89 B is correct
Which of the following threat actors is most likely to be associated with an advanced persistent threat (APT)?
A. Hacktivists
B. Nation-state actors
C. Unskilled attacker
D. Insider 

Nation state actors often have greater resources and skills, making them more of a significant threat.

90 B is correct
Erica wants to conduct an amplified DDoS attack against a system. What key step is required
as part of her attack?
A. Reversing the target’s IP address
B. Spoofing the target’s IP address
C. Conducting an on-path attack to send traffic to the target
D. Spoofing responses from the amplification system to the target

Amplification attacks typically use spoofed user Datagram Protocol UDP, queries sent to increase the volume of traffic sent in response to the target.

# 91 - 100
91. D
92. B
93. ~~A~~
94. ~~D~~
95. B
96. A
97. ~~A~~
98. D
99. ~~B~~
100. B
6/10

93 C is correct
What is the primary difference in threat vectors between agent client-based and agentless
software deployments?
A. Agentless software does not consume resources and thus cannot result in a resource
consumption-based denial-of-service condition.
B. Client-based software provides a better view of system resources and is able to manage
its resource consumption better to avoid issues.
C. Agentless software does not have an agent that may be potentially vulnerable to attack.
D. Client-based software allows for greater security because it can be patched.

Agentless software does not have an agent installed that can be targeted. That means that the server or control system is the only target for attackers. Agentless software can still consume resources as queries and actions are taken by the server or control plane.

94 B is correct
Angela reviews the authentication logs for her website and sees attempts from many different
accounts using the same set of passwords. What is this attack technique called?
A. Brute forcing
B. Password spraying
C. Limited login attacks
D. Account spinning

Password spraying is a specific type of brute force attack that uses a smaller list of common passwords for many accounts to attempt to log in. 

97 C is correct
You have discovered that there are entries in your network’s domain name server that point
legitimate domains to unknown and potentially harmful IP addresses. What best describes
this type of attack?
A. A backdoor
B. An APT
C. DNS poisoning
D. A Trojan horse

DNS poisoning occurs when false DNS information is inserted into legitimate DNS servers, resulting in traffic being redirected to unwanted or malicious sites.

99 A is true
Eric is conducting a penetration test and wants to release a malicious update for an organization’s application. The organization uses public key encryption to sign updates. What
does Eric need to deliver an update that systems will accept?
A. The private key for the signing certificate
B. A collision with the hashed value of a legitimate update
C. The public key for the signing certificate
D. A collision with the hashed value of a malicious update

In order to deliver a malicious update that uses a signing certificate, Eric will need to gain access to the private key for the signing certificate.

# 101 - 110
101. D
102. B
103. D
104. D
105. B