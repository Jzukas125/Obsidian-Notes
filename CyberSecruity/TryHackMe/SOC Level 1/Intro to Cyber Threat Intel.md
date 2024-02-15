<h3> Intro </h3>
This room will introduce cyber threat intelligence (CTI) and various frameworks used to share intelligence. As security analysts, CTI is vital for investigating and reporting against adversary attacks with organizational stakeholders and external communities.
What we want to learn:
- The basics of CTI and its classifications
- The lifecycle followed to deploy and use intelligence during threat investigations
- Frameworks and standards using in distributing intelligence

<h3> Cyber Threat Intelligence </h3>
CTI can be defined as evidence based knowledge about adversaries, including their indicators, tactics, motivations, and actionable advice against them. We need to specify the difference between data, information, and intelligence:
Data - Discrete indicators associated with an adversary, such as IP addresses, URLs or hashes
Information - A combination of multiple data points that answer questions such as "How many times have employees accessed tryhackme.com within the month"
Intelligence - The correlation of data and information to extract patterns of actions based on contextual analysis
The main goal of CTI is to understand the relationship between your operational environment and your adversary and how to defend against them. You would seek this goal by developing your own context by trying to answer the following:
	Who's attacking you?
	What are their motivations?
	What are their capabilities?
	What artifacts and indicators of compromise should you look out for?
With these questions, the threat intelligence gathered from different sources under the following categories:
	Internal
		Corporate security events such as vulnerability assessments and incident response reports
		Cyber Awareness training reports
		System logs and events
	Community
		Open web forums
		Dark web communities for cyber criminals
	External
		Threat intel feeds
		Online marketplaces
		Public sources including government data, publications, social media, financial and industrial assessments

### Threat Intelligence Classifications
Threat intel is geared towards understanding the relationship between your operational environment and your adversary. With this in mind, we can break down threat intel into the following classifications:
	Strategic Intel: High-level intel that looks into the organization's threat landscape and maps out the risk areas based on trends, patterns and emerging threats that may impact business decisions.
	Technical Intel: Evidence and artifact of an attack used. Incident response teams can use this intel to create a baseline attack surface to analyze and develop defense mechanisms
	Operational Intel: Views adversary's motives and intents. Security teams may use this intel to understand the critical assets available.

<h2> CTI Lifecycle </h2>
Threat intel is obtained from a data-churning process that transforms raw data into contextualized and action-oriented insights geared towards triaging security incidents. The transformational process follows a six-phase cycle.


Phases of the Cycle:
	Direction - Every threat intel program requires defined objects and goals, involving identifying and following parameters -- Information assets and business processes that requires defending, Potential impact to be experienced on losing the assets or through process interruptions, Sources of data nd intel to be used towards protection, tools and resources that are required to defend the assets
	Collection - Once objectives are defined, analysts will gather data to address them. Analysts will do this by using commercial, private and open-source resources available. Due to the volume of data analysts, it is recommended to automate this phase.
	Processing - Raw logs, vulnerability information, malware and network traffic usually come in different formats and may be disconnected when used to investigate an incident. This phase ensures that the data is extracted, sorted, organized, correlated with appropriate taps and presented visually in a usable format. SIEMS are valuable tools for achieving this.
	Analysis - Analysts derive insights and decide if they should investigate, define an action plan, or strengthen security controls
	Dissemination - Dividing the information up among people and translating it 
	Feedback - Communication between analysts and stakeholders to improve the threat intelligence process

CTI Standards & Frameworks
Frameworks and standards provide structures to rationalize the distribution and use of threat intel across industries.