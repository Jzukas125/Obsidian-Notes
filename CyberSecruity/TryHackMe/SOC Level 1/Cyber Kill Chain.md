<h3> Introduction </h3>
The term kill chain derives from a military concept related to the structure that consists of target identification, decision and order to attack the target, and finally the target destruction. This framework defines all the phases an attacker needs to go through in order to succeed in an attack. 
It is important to understand how the kill chain works because it will help you understand how to protect against ransomware attacks, security breaches as well as Advanced Persistent Threats (APTs).
It can be used as a baseline to help secure a network (especially helpful in an internship), basically defines a set of rules to follow (good fortune very helpful). It's also very helpful with recognizing intrusion attempts and understanding the intruder's goal and objectives. 
<h3> Reconnaissance </h3>
Reconnaissance is discovering and collecting information on the system and the victim. The reconnaissance phase is the planning phase for the adversaries. 
OSINT falls under reconnaissance (I know what OSINT is and if I forgot then I need to switch majors to business)
Looking at it from an attackers perspective, who initially doesn't know what company to attack. 
One way for an attacker to start the reconnaissance phase is to start with email harvesting.
Email harvesting is the process of obtaining email addresses from public, paid, or free services. An attacker can use email-harvesting for a phishing attack. Some reconnaissance tools are theHarvester, Hunter.io, and OSINT framework. 

<h3> Weaponization </h3>
When collecting info on a system the attacker prefers to not interact with the system and would make a weaponizer that combines malware and exploits into a deliverable payload. Most attackers automatically generate malware or buy it. While more sophisticated actors write custom malware. A payload is malicious code that attackers run on a system. 
In the weaponization phase the attacker would:
	Create an infected office document containing a malicious macro or other scripts. 
	An attacker can create a malicious payload or a very sophisticated worm, implant on usb's, and then distribute
	An attacker would choose C2 (command and control) techniques for executing commands on the victim's machine or deliver more payloads.
	An attacker would select a backdoor implant.

<h3> Delivery </h3>
Our attacker has to decide on which method will be used to transmitting the payload or malware. They could choose from:
	Phishing - Creating a fake email that would target a specific entity or multiple people. The email would usually contain the malware.
	Planting fake USB's. Could make USB's that look sophisticated by printing a company's logo and mailing them to the company, pretending to be a customer sending the USB's as a gift. 
	Water Hole Attack - A targeted attack designed to aim at a specific group of people by compromising the website they are usually visiting and then redirecting them to the malicious website of an attacker's choice. The attacker would look for known vulnerabilities for the website and try to exploit them and could encourage victims to visit by sending out "harmless" emails pointing out the malicious URL to make the attack work more efficiently. 

<h3> Exploitation </h3>
In this phase the vulnerability needs to be exploited. Our attacker gained access to the system, and will exploit software, system, or server-based vulnerabilities to escalate the privileges or move laterally through the network. 
Lateral movement refers to the techniques that malicious actor uses after gaining initial access to the victim's machine to move deeper into a network to obtain sensitive data. 

<h3> Installation </h3>
A backdoor lets an attacker bypass security measures and hide the access. The attacker would want a backdoor they can access whenever and would need to install a persistent backdoor that lets the attacker access the system he compromised in the past. A persistent back door can be achieved through:
	Installing a web shell on the webserver. A web shell is a malicious script written in web development programming languages such as ASP, PHP, or JSP used by an attacker to maintain access to the compromised system. Could be difficult to detect and might be classified as benign.
	Installing a backdoor on the victim's machine. Could use Meterpreter to install a backdoor on the victim's machine. Meterpreter is a Metasploit framework payload that gives an interactive shell from which an attacker can interact with the victim's machine remotely and execute the malicious code.
	Creating or modifying windows services. This technique is known as [T1543.003](https://attack.mitre.org/techniques/T1543/003/) on MITRE ATT&CK. An attacker can use tools like sc.exe and reg to modift service configurations. 
	Adding the entry to the "run keys" for the malicious payload in the Registry or the start up folder. By doing so, the payload will exceute each time the user logs in on the computer. According to MITRE AAT&CK there is a startup folder location for individual user accounts and a system-wide startup folder that will be checked no matter what user account logs in.
	Timestomping could also be used to avoid detection by the forensic investigator and also make the malware appear as a part of a legitimate program. 

<h3> Command & Control </h3>
After getting persistence and executing the malware on the victim's machine, the attacker opens up the C2 (command and control) channel through the malware to remotely control and manipulate the victim. The term is also known as C&C or C2 beaconing as a type of malicious communication between a C&C server and malware on the infected host. The infected host will consistently communicate with the C2 server thus the name beaconing. 
The compromised endpoint would communicate with an external server set up by an attacker to establish a command & control channel. After the connection is established, the attacker gains full control of the machine. Until recently, IRC was the traditional C2 channel used by attackers. This is no longer the case as modern security solutions can easily detect malicious IRC traffic.
The most common CS channels used are:
	The protocols on port 80 and HTTPS on port 443 - this type of beaconing blends the malicious traffic with the legitimate traffic and can help the attacker evade firewalls.
	DNS. The infected machine makes constant DNS requests to the DNS server that belongs to an attacker, this type of C2 communication is also known as DNS Tunneling (ie creating a tunnel using the DNS server)

<h3> Action on Objectives </h3>
After completing the six phases our attacker can finally achieve his goals, meaning they can take action on the original objectives. With hands-on keyboard access, the attacker can:
- Collect the credentials from the user
- Perform privilege escalation (gaining elevated access like domain administrator access from a workstation by exploiting the misconfiguration)
- Internal Reconnaissance (interacting with internal software)
- Lateral movement through the company's environment
- Collect and exfiltrate sensitive data
- Deleting the backups and shadow copies. (Shadow copy is a mircosoft tech that can create backup copies, snapshots, or volumes)
- Overwrite or corrupt data

<h3> Conclusion </h3>
Cyber kill chain can be a great tool to improve network defense. That be saying that does not mean that it is perfect and can be the only tool that we rely on. The last time it was modified was in 2011 which is the same year it was established, meaning it has security gaps from its lack of updates. The traditional cyber kill chain was designed to secure the network perimeter and protect against against malware threats, but as threats have developed drastically and adversaries are combining TTP to achieve goals more complex processes are necessary. 
TryHackMe recommends not only relying on the traditional Cyber Kill Chain model but also referring to [MITRE ATT&CK](https://attack.mitre.org/) as well as [Unified Kill Chain](https://unifiedkillchain.com/) to apply a more comprehensive approach to your defence methodologies.