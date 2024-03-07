These notes are following the Threat Intelligence Tools room on Tryhackme
This room will cover the concepts of threat intelligence and various open-source tools that will be useful. This room will help understand the basics of threat intelligence and its classifications, using UrlScan.io to scan malicious URLs, using Abuse.ch to track malware and botnet indicators, investigate phishing emails using PhishTool, and use Cisco's Talos intelligence platform for intel gathering.

# Threat Intelligence

Threat intelligence is the analysis of data and information using tools and techniques to generate meaningful patterns on how to mitigate against potential risks associated with existing or emerging threats.

To mitigate against risks we must ask ourselves first:
- Who is attacking us?
- What's their motivation?
- What are their capabilities?
- What artefacts and indicators of compromise should we look out for?

<h2> Threat Intelligence Classifications </h2>
Threat intelligence's purpose is to understand the relationship between your operational environment and your adversary. With this in mind we can break down threat intel into the following classifications:
- Strategic Intel which is high-level intel that looks into the organization's threat landscape and amps out the risk areas based on trends, patterns, and emerging threats that may impact business decisions.
- Technical intel which looks into evidence and artefacts of attack used by an adversary. Incident Response teams can use this intel to create a baseline attack surface to analyze and develop defense mechanisms.
- Tactical Intel which assesses adversaries' tactics, techniques, and procedures (TTPS). This intel can strengthen security controls and address vulnerabilities through real-time investigations
- Operational Intel  looks into an adversary's specific motives and intent to perform an attack. Security teams may use this intel to understand the critical assets available in the organization that may be targeted .

# UrlScan.io

Can be found at https://urlscan.io/

UrlScan.io is a free service developed to assist in analyzing websites. It is used to automate the process of browsing through websites to record activities and interactions. When a URL is submitted, the information recorded includes the domains and IP addresses contacted, resources requested from the domains,, a snapshot of the web page, technologies utilized and other metadata about the website. The site provides two views, the first one showing the most recent scans performed and the second one showing current live scans.

<h2> Scan Results </h2>
URL scan results usually contain:
Summary: Provides general information about the URL, ranging from the identified IP address, domain registration details, page history and a screenshot of the site
HTTP: Provides information on the HTTP connections made by the scanner to the site, with details about the data fetched and the file types received
Redirects: shows information on any identified HTTP and client-side redirects on the site
Links: Shows all identified links outgoing from the site's homepage
Behavior: Provides details of the variables and cookies found on the site. These may be useful in identifying the frameworks used in developing the site 
Indicators: Lists all IPs, domains and hashes associated with the site. These indicators do not imply malicious activity related to the site.

# Abuse.ch
Research project hosted by the institute for cybersecurity and engineering at the Bern University of Applied Sciences in Switzerland.  It was deployed to identify and track malware and botnets through several operational platforms developed under the project. The platforms are as follows:
- Malware Bazaar: A collection of malware and analysis database. The project supports malware  samples upload where security analysts can upload their malware samples for analysis and build the intelligence database, and malware hunting for hunting malware samples through setting up alerts to match various elements such as tags, signatures, YARA rules, ClamAV signatures and vendor detection.
- FeodoTracker: Shares intelligence on botnet Command and Control servers associated with dridex  emotes (aka Heodo), TrickBot, QakBot, and BazarLoader/BazarBackdoor. This is achieved by providing a data of the C&C servers that security analysts can search through and investigate any suspicious IP addresses they have come across. Additionally, they provide various IP and IOC blocklists and mitigation information to be used to prevent botnet infections.
- SSL Blacklist: Identifies and detects malicious SSL connections. From these connections, SSL certificates used by the botnet C2 servers would be identified and updated on a deny list that is provided for use. The deny list is also used to identify JA3 fingerprints that would help detect and block malware botnet C2 communications on the TCP  layer. 
- URLhaus: Shares malicious URLs used for malware distribution. As an analyst, you can search through the database for domains, URLs, hashes, and filetypes that are suspected to be malicious and validate your investigations.
- ThreatFox: Security analysts can search for, search, and export indicators of compromise associated with malware. IOCs can be exported in various formats such as MISP events, Suricata IDS Ruleset, Domain Host files, DNS response Policy zone, JSON files and CSV files.

# Phish Tool

<h2> Email Phishing </h2>
Email phishing is one of the main precursors to any cyber attack. Unsuspecting users get duped into opening and accessing malicious files and links sent to them by emails, as they appear to be legitimate. As a result, adversaries infect their victims systems, harvest credentials and personal data, and perform other actions such as financial fraud.

PhishTool seeks to elevate the perception of phishing as a severe form of attack and provide a responsive means of email security. Through email analysis, security analysts an uncover email IOCs, prevents breaches and provide forensic reports that could be used in phishing containment and training engagements. 

The main features of the community version of PhishTool are:
- Performing Email Analysis - PhishTool retrieves metadata from phishing emails and provides analysts with the relevant explanations and capabilities to follow the email's actions, attachments, and URLs to triage the situation.
- Heuristic Intelligence - OSINT is baked into the tool to provide analysts with the intelligence needed to stay ahead of persistent attacks and understand what TTPs were used to evade security controls and allow the adversary to social engineer a target.
- Classification and reporting - Phishing email classifications are conducted to allow analysts to take action quickly. Reports can be generated to provide a forensic record that can be shared.

The analysis tab is as follows:
- Headers: Provides the routing information of the email, such as source and destination email addresses
- Received Lines: Details on the email traversal process across various SMTP servers for tracing purposes
- X-Headers: Extension headers added by the recipient mailbox to provide additional information about the email
- Security: Details on email security frameworks and policies such as Sender Policy Framework (SPF) , DomainKeys Identified Mail (DKIM) and Domain-based Message Authentication, Reporting and Conformance (DMARC)
- Attachments: Lists any file attachments found in the email
- Message URLs: Associated external URLs found in the email will be found here