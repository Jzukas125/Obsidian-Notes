Notes on the MISP room in tryhackme
These notes on the tryhackme room will hopefully cover an introduction to MISP and why is was developed, Uses cases MISP can be applied to, Core features and terminologies, Dashboard navigation, event creation and management, and feeds and taxonomies.

# MISP Intro

Misp essentially gathers threat intelligences and IOCs related to malware, cyber attacks, financial fraud, or any intelligence within a community of trusted members. It allows threat information to be distributed and consumed by NIDS, log analysis tools and SIEMs.

# Using MISP

Dashboard
 - Home button: Returns to home
 - Event Actions: All the malware data entered into MISP comprises an event object described by its connected attributes.
 - Dashboard: Allows you to create custom dashboard using widgets
 - Galaxies: Shortcut to the list of MISP galaxies
 - Input Filters: Alter how users enter data into this instance.
 - Global Actions: Access to information about Misp and this instance.
 - MISP: Simple link to your baseurl
 - Name: Name (auto-generated from mail address) f currently logged in user
 - Envelope: Link to User Dashboard to consult some of your notifications and changes since the last visit. 
 - Log out: The Log oust button to end your session immediately

Event Management
	Where you create all malware investigation correlations by providing descriptions and attributes associated with the investigation. Splitting the process into three significant phases, we have: 
		Event Creation - General info about an incident or investigation. Add the description, time, and risk level deemed appropriate for the incident by clicking the Add Event button. The distribution options are as follows:
			Your organization only
			This Community only (users that are part of yout MISP community)
			Connected Communities
			All communities
		Attributes and Attachments
			For IDS: Allows the attribute to be used as an IDS signature when exporting the NIDS data unless it overrides the permitted list
			Batch Import: Several Attributes of the same type to enter
		The Analyst can also add file attachments to the event, which may include malware, report files from external analysis or simply artefacts dropped by the malware.
		Publish Event - The organization admin will review and publish these event to add them to the pool of events.

# Feeds and Taxonomies 

Feeds 
	Resources that contain indicators that can be imported into MISP and provide attributed information about security events. These feeds provide analysts and organizations with continuously updated information on threats and adversaries and aid in their proactive defense against attacks.
	MISP Feeds provide a way to:
		- Exchange threat information
		- Preview events along with associated attributes and objects
		- Select and Import events to your instance
		- Correlate attributes identified between events and feeds
	Feeds are enabled and managed by the Site Admin for the analysts to obtain information on events and indicators

Taxonomies
	A means of classifying based on standard features or attributes. On MISP, taxonomies are used to categorize events, indicators, and threat actors.

Tagging
	Information from feeds and taxonomies, tags can be placed on events and attributes to identify them based on the indicators or threats identified correctly. Tagging allows for effective sharing of threat information between users, communities and other organizations.
	Tagging Best Practices: Tags can be added to an event and attributes, Tags are also inheritable when set. It is recommended to set tags on the entire event and only include tags on attributes when they are an exception from what the event indicates. 
	Minimal Subset of Tags - 
		Traffic Light Protocol: Provides a color schema to guide how intelligence can be shared
		Confidence: Provides an indication as to whether or not the data being shared is of high quality and has been vetted so that it can be trusted to be good for immediate usage
		Origin: Describes the source of information and whether it was from automation or manual investigation
		Permissible Actions Protocol: An advanced classification that indicates how the data can be used to search for compromises within the organization.

