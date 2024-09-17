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

A test server should be identical to the production server. This can be used for functional testing as well as security testing.

# 21-30
21. A
22. ~~C~~
23. D
24. A
25. ~~A~~
26. ~~D~~
27. ~~D~~
28. ~~B~~
29. ~~C~~
30. ~~D~~
3/10

22 A is correct
Chris is following the CIS Windows Server 2022 benchmark and notices that it recommends
that Computer Configuration\Policies\Administrative Templates\Windows Components\
Search\Allow indexing of encrypted files is set to disabled. What potential issue would this
help to prevent?
A. Data leakage
B. Denial of service
C. Insecure service
D. Dark web access

Indexing encrypted files will mean that an unencrypted index is stored, potentially exposing the content of encrypted files. Disabling the indexing service for encrypted files helps to prevent them. The service is not exposed via the network, thus it is not insecure.

25 C is correct
What is the primary threat model against static codes used for multifactor authentication?
A. Brute force
B. Collisions
C. Theft
D. Clock mismatch

Static codes are typically recorded in a secure location, but if they are not properly secured, or are otherwise exposed, they can be stolen. Brute-force attempts should be detected and prevented by backoff algorithms and other techniques that prevent attacks and other techniques that prevent attacks against multifactor authentication systems.

26 C is correct
Nadine’s organization stores and uses sensitive information, including Social Security numbers. After a recent compromise, she has been asked to implement technology that can help
prevent this sensitive data from leaving the company’s systems and networks. What type of
technology should Nadine implement?
A. Stateful firewalls
B. OEM
C. DLP
D. SIEM

The best answer from this list is DLP, or data loss prevention technology. DLP is used to protect data from being exposed or leaking from a network using a variety of techniques and technology. Stateful firewalls are used to control traffic and will not detect sensitive data. SIEMs do not protect data directly. 

27 A is correct
Social login, the ability to use an existing identity from a site like Google, Facebook, or a
Microsoft account, is an example of which of the following concepts?
A. Federation
B. AAA
C. Privilege creep
D. Identity and access management

Social login is an example of a federated approach to using identities. The combination of identities is a key part of federation. IAM is a broader set of identity and access management practices. Although it may be involved it IAM is not directly described in this.

28 A is correct
Charles has configured his multifactor system to require both a PIN and a password. How
many effective factors does he have in place once he presents both of these and his username?
A. One
B. Two
C. Three
D. Four

Although it may seem like two factors, in fact he has only presented two types of things he knows along with his identity. To truly involve multifactor, he should use more than one of something you have, something you know, and something you are.

29 B is correct
Naomi is designing her organization’s wireless network and wants to ensure that the design
places access points in areas where they will provide optimum coverage. She also wants to
plan for any sources of RF interference as part of her design. What should Naomi do first?
A. Contact the FCC for a wireless map.
B. Conduct a site survey.
C. Disable all existing access points.
D. Conduct a port scan to find all existing access points

A site survey would be most appropriate as it identifies where access points should be located for best coverage and identifying existing sources of RF interference. 

30 C is correct
Charlene wants to provision her organization’s standard set of marketing information to mobile devices throughout her organization. What MDM feature is best suited to this task?
A. Application management
B. Remote wipe
C. Content management
D. Push notifications

Mobile device management suites often provide the ability to manage content on devices as well as applications. Using content management tools can allow Charlene to provision files, documents, and media to the devices that staff members in her organization are issued.

# 31- 40
31. ~~A~~
32. C
33. ~~C~~
34. B
35. D
36. C
37. A
38. ~~D~~
39. ~~D~~
40. B
6/10

31 C is correct
Denny wants to deploy antivirus for his organization and wants to ensure that it will stop the
most malware. What deployment model should Denny select?
A. Install antivirus from the same vendor on individual PCs and servers to best balance visibility, support, and security.
B. Install antivirus from more than one vendor on all PCs and servers to maximize
coverage.
C. Install antivirus from one vendor on PCs and from another vendor on the server to provide a greater chance of catching malware.
D. Install antivirus only on workstations to avoid potential issues with server performance

Diversity is the best way to catch the most malware and installing different on servers and pcs will catch the most, while installing different ones on the same system is rarely recommended.

33 A is correct
You’re outlining your plans for implementing a wireless network to upper management.
What wireless security standard should you adopt if you don’t want to use enterprise authentication but want to provide secure authentication for users that doesn’t require a shared
password or passphrase?
A. WPA3
B. WPA
C. WPA2
D. WEP

WPA3 supports SAE or simultaneous authentication of equals, providing a more secure way to authenticate that limits the potential for brute forcing. WPA is not as secure as WPA2, and WEP is the oldest and least secure.

38 B is correct
Endpoint detection and response has three major components that make up its ability to
provide visibility into endpoints. Which of the following is not one of those three parts?
A. Data search
B. Malware analysis
C. Data exploration
D. Suspicious activity detection

EDRs do not do malware analysis

39 A is correct
Carl has been asked to set up access control for a server. The requirements state that users
at a lower privilege level should not be able to see or access files or data at a higher privilege
level. What access control model would best fit these requirements?
A. MAC
B. DAC
C. RBAC
D. SAML

Mandatory Access control MAC, is the correct answer. It will not allow lower privileged users to even see the data at a higher privilege. Discretionary Access control DAC, has each data owner configure their own security. Role based access control RBAC, could be configured to meet the needs, but its not the best solution. Security assertion markup language is not an access control model.

# 41 - 50
41. C
42. ~~A~~
43. B
44. ~~C~~
45. ~~C~~
46. B
47. ~~C~~
48. ~~A~~
49. A
50. C
5/10

42 C is correct
Claire is concerned about an attacker getting information regarding network devices and
their configuration in her company. Which protocol should she implement that would be
most helpful in mitigating this risk while providing management and reporting about
network devices?
A. RADIUS
B. TLS
C. SNMPv3
D. SFTP

If Claire is using SNMP (simple network management protocol) to manage and monitor her network devices, she should make sure she is using SNMPv3 and that it is properly configured. SNMPv3 can provide information about the status and configuration of her network devices. Remote Authentication Dial in user service (RADIUS) might be used to authenticate to the network, but Transport layer security and SSH File Transfer Protocol are not specifically used for the purposes described.

44 B is correct
Tara is concerned about staff in her organization sending email with sensitive information
like customer Social Security numbers (SSNs) included in it. What type of solution can she
implement to help prevent inadvertent exposures of this type of sensitive data?
A. FDE
B. DLP
C. S/MIME
D. POP3S

Data loss prevention tools allow sensitive data to be tagged and monitored so that if a user attempts to send it, they will be notified, administrators will be informed, and if necessary, the data can be protected using encryption or other protection methods before it is sent. S/MIME and POP3S would protect mail being retrieved from a server but would not prevent the SSNs from being sent.

45 A is correct
Mason is responsible for security at a company that has traveling salespeople. The company has been using ABAC for access control to the network. Which of the following is an issue that is specific to ABAC and might cause it to incorrectly reject logins?
A. Geographic location.
B. Wrong password.
C. Remote access is not allowed by ABAC.
D. Firewalls usually block ABAC.

Attribute-based access control (ABAC) looks at a group of attributes, in addition to the login username and password, to make decisions about whether or not to grant access. One of the attributes examined is the location making geo location the answer.

47 D is correct
Frank is a security administrator for a large company. Occasionally, a user needs to access a specific resource that they don’t have permission to access. Which access control methodology would be most helpful in this situation?
A. Mandatory access control (MAC)
B. Discretionary access control (DAC)
C. Role-based access control
D. Rule-based access control

Rule based access control applies a set of rules to an access request. Based on the application of the rules, the user may be given access to a specific resource that they were not explicitly granted permission to.

48 D is correct
Oliver needs to explain the access control scheme used by both the Windows and Linux filesystems. What access control scheme do they implement by default?
A. Role-based access control
B. Mandatory access control
C. Rule-based access control
D. Discretionary access control

Both the windows and Linux filesystems work based on a discretionary access control scheme where file and dictionary owners can determine who can access, change, or otherwise work with files under their control. 

# 51-60
51. ~~C~~
52. ~~D~~
53. ~~C~~
54. ~~A~~
55. B
56. ~~C~~
57. B
58. ~~B~~
59. ~~D~~
60. A
3/10

51 B is correct
A companywide policy is being created to define various security levels. Which of the following systems of access control would use documented security levels like Confidential or Secret
for information?
A. RBAC
B. MAC
C. DAC
D. BAC

Mandatory Access Control (MAC) is based on documented security levels associated with the information being accessed. Role based (RBAC) is based on the role, Discretionary (DAC) lets the data owner set control. BAC is not an access control model

52 A is correct
Users in your network are able to assign permissions to their own shared resources. Which of
the following access control models is used in your network?
A. DAC
B. RBAC
C. MAC
D. ABAC

DAC allows data owners to assign permissions.

53 A is correct
Cynthia is preparing a new server for deployment, and her process includes turning off
unnecessary services, setting security settings to match her organization’s baseline configurations, and installing patches and updates. What is this process known as?
A. OS hardening
B. Security uplift
C. Configuration management
D. Endpoint lockdown

OS hardening is the process of securing an operating system by patching. 

54 D is correct
John is performing a port scan of a network as part of a security audit. He notices that the
domain controller is using secure LDAP. Which of the following ports would lead him to that
conclusion?
A. 53
B. 389
C. 443
D. 636

Secure Lightweight Directory Access Protocol (LDAPS) uses port 636 by default. DNS uses port 53, LDAP uses 389, and secure HTTP uses port 443.

56 A is correct
Gary is designing his cloud infrastructure and needs to provide a firewall-like capability for
the virtual systems he is running. Which of the following cloud capabilities acts like a virtual
firewall?
A. Security groups
B. Dynamic resource allocation
C. VPC endpoints
D. Instance awareness

Security gaps are a virtual firewall for instances, allowing rules to be applied to traffic between instances. Dynamic resource allocation is a concept that allows resources to be applied as they are needed, including scaling up and down infrastructure and systems on the fly. 

59 A is correct
Lucas is looking for an XML-based open standard for exchanging authentication
information. Which of the following would best meet his needs?
A. SAML
B. OAuth
C. RADIUS
D. NTLM

Security Assertion markup language (SAML) is an XML based open standard format for exchanging authentication and authorization data between parties. 

# 61 - 70
61. C
62. C
63. D
64. ~~B~~
65. ~~D~~
66. ~~C~~
67. ~~D~~
68. D
69. B
70. ~~A~~
5/10

64 D is correct
Jessica wants to review the network traffic that her Windows system has sent to determine if
a file containing sensitive data was uploaded from the system. What Windows log file can she
use to find this information?
A. The application log
B. The network log
C. The security log
D. None of the above

Windows does not log network traffic at a level of granularity that will show if a file has been uploaded that allows for Jessica to determine if the files are sent from a windows system.

65 C is correct
What term is used to describe the documentation trail for control, analysis, transfer, and final disposition of evidence for digital forensic work?
A. Evidence log
B. Paper trail
C. Chain of custody
D. Digital footprint

