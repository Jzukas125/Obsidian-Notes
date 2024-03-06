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
