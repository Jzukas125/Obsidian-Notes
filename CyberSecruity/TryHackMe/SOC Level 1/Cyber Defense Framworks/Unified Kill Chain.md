#TryHackMe 
<h3> Intro </h3>
Understanding the behaviors, objectives, and methodologies of a cyber threat is a vital step to establish a strong cybersecurity defense. We will be introduced to the UKC framework that is used to help understand how cyber attacks occur.

<h3> What is a Kill Chain </h3>
Originally from the military, a kill chain is a term used to explain the various stages of an attack. In the realm of cyber security a kill chain is used to describe the method attacks use to approach and intrude a target. 

<h3> What is "Threat Modeling" </h3>
Threat modeling is a series of steps used to improve the security of a system. Threat modeling is about identifying risk and boils down to:
1. Identifying what systems and applications need to be secured and what function they serve
2. Addressing what vulnerabilities and weaknesses these systems and applications may have and how they could potentially be exploited.
3. Creating a plan of action to secure the systems
4. Putting in policies to secure these systems
Threat modeling is an important procedure in reducing the risk within a system or application, as it creates a high-level overview of an organization's IT assets and the procedures to resolve vulnerabilities. 

<h3> Introducing the Unified Kill Chain </h3>
The unified kill chain aims to complement with other kill chain frameworks suck as Lockheed's MITRE's ATT&CK. The UKC states that there are 18 phases to an attack: Everything from reconnaissance to data exfiltration and understanding an attacker's motive. These phases have grouped together in this room into a few areas of focus for brevity, which will be detailed in the remaining tasks. 
![[Pasted image 20231109100754.png]]
Benefits of the UKC Framework  -  How do other Frameworks Compare
Modern (released in 2017 update in 2022) - Others were released in 2013
UKC is extremely detailed - other frameworks often have a small handful of phases
UKC covers an entire attack - other frameworks cover a limited amount of phases
UKC highlights a much more realistic attack scenario - other frameworks do not account for attackers to move back and fourth between various phases during an attack

<h3> Phase: In (initial foothold) </h3>
The main focus of this series of phases is for an attacker to gain access to a system. An attacker will employ numerous tactics to investigate the system for potential vulnerabilities that can be exploited to gain a foothold in the system. This series of phases also accommodates for an attacker creating a form of persistence. 
	Reconnaissance
		This phase describes techniques that an adversary employs to gather information relating to their target. This can be achieved through means of passive and active reconnaissance. The information gathered during this phase is used all throughout the later stages of the UKC.
	Weaponization
		This phase of the UKC describes the adversary setting up the necessary infrastructure to perform the attack. For example, this could be setting up a command and control server or a system capable of catching reverse shells and delivering payloads to the system.
	Social Engineering 
		The phase of the UKC describes techniques that an adversary can employ to manipulate employees to perform actions that will aid in the adversaries attack.
	Exploitation
		This phase of the UKC describes how an attacker takes an advantage of weaknesses or vulnerabilities present in a system.
	Persistence
		This phase of the UKC describes techniques an adversary yes to maintain access to a system they have gained an initial foothold on.
	Defense Evasion
		This section of the UKC is incredibly valuable specifically because it's used to understand the techniques an adversary uses to evade defensive measures put in place in the system or network. For example this could be, Web application firewall, network firewalls, and the intrusion detection systems.
	Command & Control 
		The command & control phase of the UKC combines the efforts an adversary made during the Weaponization stage of the UKC to establish communications between the adversary and target system.
	Pivoting
		Pivoting is the technique an adversary uses to reach other systems within a network that are not otherwise accessible. There are often many systems in a network that are not directly reachable and often contain valuable data or have weaker security.

<h3> Phase: Through </h3>
This phase follows a successful foothold being established on the target network. An attacker would seek to gain additional access and privileges to systems and data to fulfil their goals. 
	Pivoting 
		Once the attacker gains access, they would use this as their staging site and a tunnel between their command operations and victim's network. The system would also be used as their distribution point for all malware and backdoors at later stages.
	Discovery
		The adversary would uncover information about the system and the connected network. The knowledge would include user accounts, permissions granted, applications and software, web browser activity, files,, directories and network shares, and system configurations. 
	Privilege Escalation 
		The attacker would try to gain more prominent permissions within the pivot system. They would leverage the information on the accounts present with vulnerabilities and misconfigurations found to elevate their access to one of the following superiors levels: System/root, local admin, user account with admin like access, 
	Execution 
		Recall when the adversary set up their attack infrastructure. Once the attack has access to the system, they would use it as their staging site and a tunnel between their command operations and the victim's network. The system would also be used as the distribution point for all malware and backdoors at later stages and weaponized payloads?
	Credential Access 
		Working hand in hand with the Privilege escalation stage, the adversary would attempt to steal account names and passwords through various methods, including keylogging and credential dumping. This makes them harder to detect during their attack as they would be using legitimate credentials.
	Lateral Movement
		With the credentials and elevated privileges, the adversary  would seek to move through the network and jump onto other targeted systems to achieve their primary objective.
<h3> Phase: Out </h3>
This phase wraps up the journey of an adversary's attack on an environment, where they have critical asset access and can fulfill their attack goals. 
	Collection
		The attacker will be seeking to gather all the valuable data of interest. This, in turn, compromises the confidentiality of the data and would lead to the next attack stage.
	Exfiltration
		To elevate their compromise, the adversary would seek to steal, which would be packaged using encryption measures and compression to avoid any detection. The C2 channel and tunnel deployed in the earlier phases will come in handy during this process.
	Impact 
		If the adversary seeks to compromise the integrity and availability of the data assets, they would manipulate, interrupt or destroy these assets. The goal is to disrupt business and operational process and may involve removing account access, disk wipes, and data encryption.
	Objectives
		With all the power and access to the systems and network, the adversary would seek to achieve their strategic goal for the attack.
<h3> Conclusion </h3>
The UKC is the modern extension of other frameworks, such as Lockheed's cyber kill chain framework. 