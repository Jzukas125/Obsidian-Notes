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
42. A
43. C
44. B
45. B
46. D
47. C
48. C
49. A
50. B

