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
- Operational Intel  looks into an adversary's specifc motive