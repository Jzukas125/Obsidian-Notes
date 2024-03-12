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
			