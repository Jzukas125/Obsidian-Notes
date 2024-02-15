# Security policies

Security Policy guidelines
	what rules are you following to provide CIA?
	High level strategies have data storage requirements, and security event procedures
	Detailed security goals have appropriate Wi-Fi usage
	Security policies answer the "what" and the "why"

Information Security Policies
	The big list of all security-related policies
	compliance requirements 
	detailed security procedures
	a list of role and responsibilities 
	organization must enforce policy 

Acceptable Use Policies (AUP)
	What is acceptable use of company assets? has detailed documentation
	Covers many topics such as internet use, telephones, computers, and mobile devices
	Used by an organization to limit legal liability 

Business Continuity 
	not everything goes according to plan
	we rely on our computer systems
	There needs to be an alternative like manual transactions, paper receipts, and phone calls for transaction approvals 
	These must be documented and tested before a problem occurs

Disaster recovery plan
	if a disaster happens, IT should be ready
	Disasters are many an varied such as natural disasters, technology or system failures
	a comprehensive plan for recovery location, data recovery method, application restoration, IT team and employee availability

Security incidents
	user clicks an email with malware
	DDoS
	Confidential information is stolen

Incident response roles
	Incident response team
	IT security management has corporate support
	compliance officers has intricate knowledge of compliance rules
	Technical staff
	User community sees everything

NIST SP800-61
	Computer Security Incident Handling Guide
	Incident response lifecycle is preparation, detection and analysis, containment, eradication, recovery, and post-incident activity

SDLC
	Systems development life cycle
	Many ways to get from idea to app and many moving parts, customer requirements, keep the process on schedule, and stay in budget
	There's no "best way" but it helps to have a framework and there are many options
![[Pasted image 20240205192703.png]]

Change management
	how to make a change, upgrade software, change firewall configuration, and modify switch ports
	One of the most common risks in the enterprise and occurs very frequently
	Often overlooked or ignored 
	Have clear policies 
	sometimes extremely difficult to implement 

# Security standards

Security standards
	a formal definition for using security technologies and processes
	may be written in house
	many standards are already available

Password
	what makes a good password?
	define acceptable authentication methods
	create policies for secure password resets
	other password policies

Access control
	how does an organization control access to data?
	Define which access control types can be used
	Determine how a user gets access
	Document how access may be removed

Physical Security
	rules regarding physical security
	granting physical access
	define specific physical security systems
	additional security concerns

Encryption
	define specific standards for encrypting and securing data
	password storage 
	Data encryption minimums 

# Security Procedures

Change management 
	formal process for managing change
	nothing changes without the process
		Determine the scope of the change
		Analyze the risk associated with the change
		Create a plan
		Get end-user approval
		Present the proposal to the change control board
		Have a backout plan if the change doesn't work
		Document the changes

Onboarding
	bring a new person into the organization 
	IT agreements need to be signed
	Create accounts 
	Provide required IT hardware

Offboarding
	all good things come to an end
	the process should be pre-planned
	What happens to the hardware?
	What happens to the data?
	Account information is usually deactivated

Playbooks
	conditional steps to follow: a broad process
	Step-by-step set of processes and procedures
	Often integrated with a SOAR platform which is a Security Orchestration, Automation, and Response, integrate third party tools and data sources, make security teams more effective

Monitoring and revision
	IT security is constantly changing with processes and procedures also must change
	Update to security posture 
	Change to an individual procedure can update the playbooks, include additional checks
	New security concerns can protect against emerging threats 

Governance structures 
	Boards are a panel of specialists that set the tasks or requirements for the committees
	Committees are subject-matter experts and determines the next steps for a topic at hand

Governance structures 
	Government entities are a different kind of machine with legal concerns, administrative requirements, political issues and are often open to the public
	Centralized/Decentralized are the source of the processes and procedures, Centralized governance is located in one location with a group of decision makers while decentralized governance spreads the decision-making process around to other individuals or locations 

# Security Considerations 

Regulatory
	regulations are often mandated with security processes are usually a foundational consideration
	Sarbanes-Oxley Act (SOX) is the public company accounting reform and investor protection act of 2002
	The HIPPA has extensive health care standards for storage, use, and transmission of health care information

Legal 
	the security team is often tasked with legal responsibilities such as reporting legal activities and holding data required for legal proceedings
	Security breach notifications are a legal requirement in many jurisdictions
	Cloud computing can make this challenging with data moving between jurisdictions  without human intervention
	The security team must follow legal guidelines

Industry 
	the industry may require specific security considerations
	Electrical power and public utilities with isolated and protected system controls
	Medical is highly secure data storage and access logs

Geographical security
	local/regional has city and state government records
	national has federal govts and national defense, multi-state organizations, and state secrets remain secret
	Global are large multinational companies with global financial markets and legal concerns vary widely

# Data roles and responsibilities 

Data responsibilities
	High-level data relationships that are organizational responsibilities, not always technical 
	Data owner are accountable for specific data, often a senior officer, VP of sales owns the customer relationship data and a treasurer owns the financial information

Data roles
	Data controller manages the purposes and means by which personal data is processed
	Data processor processes data on behalf of the data controller which is often a third-party or different group
	Payroll controller and processor has the payroll department (data controller) defines payroll amounts and timeframes 
	Payroll company (data processor) processes payroll and stores employee information 

Data roles 
	data custodian/steward is responsible for data accuracy, privacy, and security
	works directly with the data that associates sensitivity labels to the data and ensures compliance with any applicable laws and standards, manages the access rights to the data, and implements security controls

# Risk management

Risk identification
	the only certainty is uncertainty
	an important part of an organization
	Risk management

Performing a risk assessment
	not all risk requires constant evaluation or it might be required to always assess the amount of risk
	One-time the assessment may be part of a one-time project 
	Continuous assessments may be part of an existing process and change control requires a risk assessment as part of the change

Ad hoc assessments
	an organization may not have a formal risk assessment process and perform an assessment when the situation requires 
	CEO is back from a conference and wants to know if the organization is protected from a new attack type
	A committee is created and the risk assessment proceeds and once the assessment is complete, the committee is disbanded and there may not be a need to investigate this specific risk again

Recurring assessments
	recurring assessments where an evaluation occurs on standard intervals
	an internal assessment is performed every three months at the beginning of the quarter 
	A mandated risk assessment is required by certain organizations, some legal requirements will mandate an assessment, and PCI DSS requires annual risk assessments

# Risk analysis

Qualitative risk assessment
	identify significant risk factors and ask opinions about the significance and display visually with traffic light grid or similar method 

![[Pasted image 20240205211843.png]]

Quantitative risk assessment
	Annualized Rate of Occurrence ARO is how likely events will happen
	Asset Value (AV) is the value of the asset to the organization and includes the cost of the asset, the effect on company sales, potential regulatory fines, etc.
	Exposure Factor (EF) is the percentage of the value lost due to an incident losing a quarter is .25 and losing the entire asset is 1.0
	SLE (single loss expectancy)
	what i the monetary loss if a single event occurs 
	Asset value * Exposure factor
	Laptop stolen = $1000 * 1.0 = 1000
	ALE annualized loss expectancy
	The business impact can be more than monetary

Impact
	Life the most important consideration
	Property risk to building and assets
	Safety - some environments are too dangerous to work
	Finance is the resulting financial cost 

Likelihood and probability
	risk likelihood is a qualitative measurement of risk 
	risk probability is a quantitative measurement of risk and is a statistical measurement and can be based on historical 
	Often considered similar in scope and can be used interchangeably in casual conversation 

Risk appetite and tolerance 
	Risk appetite is a broad description of risk-taking deemed acceptable 
	Risk appetite posture is a qualitative description for readiness to take risk
	Risk tolerance is an acceptable variance is usually larger from the risk appetite

Risk register
	Every project has plan, but also has risk, identify and document the risk associated with each step, apply possible solutions to the identified risks, monitor the results
	Key risk indicators identify risks that could impact the organization
	Risk owners - each indicator is assigned someone to manage the risk
	Risk threshold - the cost of mitigation is at least equal to the value gained by mitigation

# Risk Management Strategies

Risk management strategies
	Transfer moves the risk to another party 
	Accept a business decision; we'll take the risk
	Accept with exemption a security policy or regulation cannot be followed 
	May be based on available security controls, size of the organization, total assets, etc
	Accept with exception with internal security policies are not applied, monthly security updates must be applied within 3 calendar days
	The monthly updates cause a critical software package to crash
	An exception is made to the update timeframe 

Risk management strategies 
	Avoid - stop participating in a high risk activity
	Mitigate - decrease the risk level, invest in security systems

Risk reporting
	a formal document that identifies risk and has detailed information for each risk
	Usually created for senior management to make decisions regarding resources, budgeting, and additional security tasks
	Commonly includes critical and emerging risks the most important considerations

# Business Impact Analysis

Recovery 
	Recovery time objective (RTO) - get a service up and running quickly and back to a particular service level
	Recovery point objective - how much data loss is acceptable? bring the system back how far does the data go
	Mean time to repair (MTTR) - average time required to fix an issue, includes time spent diagnosing the problem, important metric for determining the cost and time associated with unplanned outages
	Mean time between failures (MTBF) - the time between outages, can be used as a prediction or calculated based on historical performance, total uptime / number of breakdowns, statistically plan for possible outages

# Third-Party Risk Assessment 

Third-party risk
	every organization works with vendors such as with payroll, customer relationship management, email marketing, travel, and raw materials
	Important company data is often shared and may be required for cloud services
	perform a risk assessment 
	Use contracts for clear understanding to make sure everyone understand the expectations
	Use the contract to enforce a secure environment

Penetration testing
	pentest to simulate an attack
	similar to vulnerability scanning
	often a compliance mandate may include a legal requirement
	regular pen testing by a 3rd party is very specialized 

Rules of engagement
	An important document defines purpose and scope, and makes everyone aware of the test parameters
	Type of testing and schedule such as on-site physical breach, internal test, external test
	The rules such as IP address ranges, emergency contacts, how to handle sensitive information, in-scope and out-of-scope devices or application

Right to audit clauses
	common to work with business partners such as data sharing and outsourcing
	Third-party providers can hold all of the data, and manage internet access
	Right-to-audit should be in the contract, a legal agreement to have the option to perform a security audit at any time, everyone agrees to the terms and conditions, ability to verify security before a breach occurs

Evidence of internal audits
	Evaluate the effectiveness of security controls and have a third-party perform an audit
	May be required for compliance
	Check for security controls and processes such as access management, off boarding, password security, VPN controls, etc
	Always an opportunity for improvement
	Perform at a reasonable frequency 

Supply chain analysis
	the system involved when creating a product involves organizations, people, activities, and resources
	Supply chain analysis can get a product or service from supplier to customer, evaluate coordination between groups, identify areas of improvement, Assess the IT systems supporting the operation, document the business process changes 
	Software update installs malware: March-June 2020
		Announced December 2020 by SolarWinds, Malware deployed with a valid SolarWinds digital signature, At least 18,000 of 300,000 customers potentially impacted

Independent assessments 
	Bring in a smart person or team to evaluate security and provide recommendations
	Specialists in their field
	Can provide options that haven't been considered

Vendor selection process
	Due diligence check a company before doing business and investigate and verify information
	Conflict of interest is a personal interest that could compromise judgement, a potential partner also does business with your largest competitor

Vendor Monitoring
	ongoing management of the vendor relationship
	Reviews should occur on a regular basis
	Different vendors may be check for different indicators
	Assign a person to be in charge of the vendor relationship

Questionnaires
	important part of due diligence and ongoing vendor monitoring
	Security related questions such as what is the vendor's due diligence process?, what plans are in place for disaster recovery?
	Results are used to update a vendor risk analysis

# Agreement Types

Common agreements
	Service level agreement (SLA) are minimum terms for services provided 
	Contract with an internet service provider is SLA no more than four hours of unscheduled downtime, technician will be dispatched, and may require customer to keep spare equipment on-site
	Memorandum of Understanding (MOU) have both sides agree in general to contents of the memorandum, usually states common goals, but not much more
	Memorandum of Agreement (MOA) is a step above a MOU, both sides conditionally agree to the objectives, can also be a legal document, even without a legal language

Common Agreements Continued
	Master Service Agreement (MSA) is a legal contract and agreement of terms, a broad framework to cover later transactions, many detailed negotiations happen here
	Work order (WO) / Statement of Work (SOW) is a specific list of items to be completed, used in conjunction with a MSA, details the scope of the job, location, deliverables schedule, acceptance criteria, and more

NDA
	confidentiality agreement
	protects confidential information 
	unilateral, bilateral, or multilateral
	Formal contract

Common agreements
	Business Partners Agreement (BPA)
	Going into business together 
	Decision making
	Prepare for contingencies

# Compliance

Compliance
	meet the standards of laws, policies, and regulations
	A healthy catalog of rules across many aspects of business and life
	Penalties
	Scope

Compliance reporting
	internal monitor and report on organizational compliance efforts 
	Late organizations have a CCO (central compliance officer)
	External documentation required by external or industry regulations 

Regulatory compliance
	Sarbanes-Oxley Act is the public company accounting reform and investor protection Act of 2002
	The health insurance portability and accountability act (HIPPA) big health care protections act
	Gramm-Leach-Bliley Act of 1999 (GLBA) is disclosure of privacy information from financial institutions

HIPPA non compliance fines and sanctions
	fine of up to 50,000 dollars or up to a year in prison or both (Class 6 felony)
	Under false pretenses a fine of up to 100,000 dollars, up to 5 years in prison or both (Class 5 felony)
	Intent to sell, transfer or use individually identifiable health information for commercial advantage, personal gain, or malicious harm, a fine up to 250,000 or up to 10 years in prison or both (Class 4 felony)
	Civil fines; maximum is $100 for each violation, with the total amount not to exceed 25,000 for all violations of an identical requirement or prohibition during a calendar year 

Reputational damage
	getting hard isn't a great look as organizations are often required to disclose 
	stock prices drop, at least for the short term

Other consequences 
	loss of license such as significant economic sanction, organization cannot sell products, others cannot purchase from a sanctioned company, expensive to re-license
	Contractual impacts with some business deals may require a minimum compliance level, without compliance, the contract may be in breach and may be resolved with or without a court of law 

Compliance monitoring
	ensure compliance in day-to-day operations
	Due diligence/care is a duty to act honestly and in good faith
	Attestation and acknowledgement where someone must sign off on formal compliance documentation

Compliance monitoring
	internal and external monitor compliance with internal tools, provide access or information to third-party participants and may require ongoing monitoring of third party operations
	Automation is a must have for large organizations and can be quite different across vertical markets, many third party monitoring systems, collect data from people and systems, and compile the data and report

# Privacy

Privacy legal implications
	a constantly evolving set of guidelines 
	Local / regional with state and local governments set privacy limits
	National privacy laws for everyone in the country
	Global many countries are working together for privacy

GDPR - General Data Protection Regulation

EU regulation
	Data protection and privacy for individuals in the EU
	Controls export of personal data and users can decide where their data go
	Gives data subjects control

Data subject 
	any information relating to an identified or identifiable natural person 
	This includes everyone's Name, ID number, address information, genetic makeup, physical characteristics, location data, etc
	You are the data subject
	Laws and regulations where privacy is ideally defined from the perspective of the data subject

Data responsibilities
	High-level data relationships with organizational responsibilities, not always technical
	Data owner is accountable for specific data, often a senior officer 
	VP of sales owns the customer relationship data
	Treasurer owns the financial information

Data roles
	data controller manages the purposes and means by which personal data is processed 
	data processor processes data on behalf of the data controlled and is often a third-party or different group
	Payroll controller and processor has the payroll department (data controller) defines payroll amounts and timeframes
	Payroll company (data processor) processes payroll and stores employee information

Data inventory and retention 
	What data does your organization store? and you should store document your data inventory
	Data inventory is a listing of all managed data with owner, update frequency, format of the data
	Internal use use with project collaboration, IT security, and data quality checks
	External use can select data to share publicly and follow existing laws and regulations

# Audits and Assessments

Audits and assessments 
	Not just for taxes
	Cybersecurity audits examines the IT infrastructure, software, devices, etc
	checks for effectiveness of policies and procedures
	Find vulnerabilities before the attackers 
	Can be performed internally or by third parties
	Attestation - provides an opinion of truth or accuracy of a company's security positioning 

Internal Audits
	audits aren't just for third-parties
	compliance checking if your organization complies with regulatory or industry requirements
	Audit committee oversees risk management activities and all audits start and stop with the committee 
	Self-assessments have the organization perform their own checks and consolidate the self-assessments into ongoing reports 

External Audits
	regulatory requirements are an independent third-party may be required to perform the audit
	Audit type and frequency are often based on the regulation
	Examinations, Audits will often require hands-on research
	View records, compile reports, gather additional details
	Assessment, audit will asses current activities and may also provide recommendation for future improvements 

# Penetration Testing

Physical penetration testing 
	Operating system security can be circumvented by physical means, modify the boot process, boot from other media, and modify or replace OS files
	Physical security is key
	Assess and test physical security, can you enter without a key?

Pentesting perspectives
	offensive, attacks the systems and look for vulnerabilities
	defensive, identify attacks in real time and prevent unauthorized access
	integrated, create an ongoing process, identify and patch exploitable systems and services

Working knowledge
	how much do you know about the test?
	known environment which gives full disclosure
	Partially known environment which is a mix of known and unknown
	Unknown environment where the pentest know nothing about the systems under attack
	"Blind" test

Reconnaissance
	need information before the attack and you can't rush blindly into battle
	Gathering a digital footprint and learn everything you can
	Understand the security posture
	Minimize the attack area and focus on key systems
	Create a network map to identify routers, networks, and remote sites

Passive reconnaissance
	learn as much as you can from open sources
	Social media
	Corporate web site
	Online forums, Reddit
	Social engineering
	Dumpster diving
	Business organizations

Active reconnaissance
	trying the doors 
	visible on network traffic and logs
	Ping scans, port scans
	DNS queries
	OS scans, OS fingerprinting
	Service scans 

# Security Awareness

Phishing campaigns 
	how many employees would click a link in a phishing email?
	Many companies will perform their own phishing campaign
	An automated process for centralized reporting for incorrect clicks, users can receive immediate feedback and security training, and some organizations will schedule in-person training

Phishing campaigns
	recognize a phishing attempt usually has spelling and grammatical errors, domain name and email are inconsistent, unusual attachments, and requests for personal information
	Respond to reported suspicious messages where email filtering can get the worst offenders, never click a link in an email, never run an attachments from an email, all organizations should have a process for reporting phishing

Anomalous behavior recognition
	Risky behavior like modifying hosts file, replacing a core OS file, and uploading sensitive files 
	Unexpected behavior can logon from another country and increase in data transfers
	Unintentional behavior such as typing the wrong domain name, misplacing USB drives, and misconfiguring security settings 

Reporting and monitoring
	track and analyze security awareness metrics 
	Initial, first occurrence is an opportunity for user training and work towards avoiding the issue in the future
	recurring is the value of long term monitoring, identifies high-frequency security issues, and helps users with multiple occurrences 

Development
	Create a security awareness team to determine roles for training, monitoring, and policy creation
	Establish a minimum awareness level such as information delivery and depth of training based on job function
	Integrate compliance mandates such as PCI DSS, HIPPA, GDPR
	Define metrics can assess the performance of security awareness programs and make updates in lower-performing areas

Execution 
	Create the training materials to provide to users in different forms
	Document success measurements 
	Identify the stakeholders and provide on going metrics and performance data
	Deploy the training efforts with ongoing monitoring, usually with an automated reporting system

# User training 

Security awareness training 
	before providing access, train your users
	specialized training with each user role has unique security responsibilities 
	also applies to third-parties
	detailed documentation and records 

User guidance and training 
	Policy/Handbooks document all security requirements, provide access online in policy guidelines, and reference the policies in the employee handbook
	Situational awareness where users should always be looking for threats 
	Insider threat is difficult to guard against, add multiple approvals for critical processes, monitor files and systems as much as possible, and it should be very difficult to make an unauthorized change
	Password management have many standards to choose from, guide users with standard requirements and this is often controlled using technology
	Removable media and cables such as an unknown USB drives could contain malware
	Social engineering has extensive and ongoing training

User guidance and Training
	Operational security to view security from the attacker's perspective
	Hybrid/remote work environments, working at home brings unusual security risks, no access to family and friends, additional endpoint security, and security policies for VPN access