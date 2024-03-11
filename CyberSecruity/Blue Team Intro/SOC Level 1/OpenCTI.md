These notes are on the room OpenCTI on TryHackme and it will cover the concepts and usage of OpenCTI, an open-source threat intelligence platform. The room will help us understand the answer to the following questions:
- What is OpenCTI and how is it used?
- How would I navigate through the platform?
- What functionalities will be important during a security threat analysis?
It is suggested that we visit the MITRE ATT&CK Framework TheHive, MISP, and Threat Intelligence Tools rooms before we continue.

# Introduction to OpenCTI

Cyber Threat intelligence is typically a managerial mystery to handle, with organizations battling with how to input, digest, analyze, and present threat data in a way that will make sense. It is clear from the rooms above that threat intelligence truly is a beast to handle and Open CTI is a tool that is helpful in conquering said beast. 

# OpenCTI 

OpenCTI uses a variety of knowledge schemas in structuring data, the main one being the structured threat information expression standards. STIX is serialized and standardized language format used in threat intelligence exchange. It allows for the data to be implemented as entities and relationships, effectively tracing the origin of the provided information.
![[Pasted image 20240309105420.png]]
Image from https://tryhackme.com/room/opencti

The highlight services include:
- GraphQL API - The API connects clients to the database and the messaging system
- Write Workers - Python processes utilized to write queries asynchronously from the RabbitMQ messaging system
- Connectors - Another set of python processes used to ingest, enrich or export data on the platform. These connectors provide the application with a robust network of integrated systems and frameworks to create threat intelligence relations and allow users to improve their defense tactics. 
According to OpenCTI, connectors fall under the following classes of:
![[Pasted image 20240309105901.png]]

OpenCTI is separated into different areas along with its GUI and I will attempt to explain in these notes.

![[Pasted image 20240310151501.png]]

- Dashboard:  Showcases various visual widgets summarizing the threat data ingested into OpenCTI. Widgets on the dashboard showcase the current state of entities ingested on the platform via the total number of entities.
- Activities: Located on the left side panel under the Open CTI logo
	- Analysis: contains the input entities in reports analysed and associated external references. Reports are central to OpenCTI as knowledge on threats and events are extracted and processed.
	- Events: 