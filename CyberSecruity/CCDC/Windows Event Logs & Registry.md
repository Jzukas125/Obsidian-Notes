# Introduction
Windows Event Log: An in-depth record of events related to the system, security, and application stored on a Windows operating system.
Windows Registry: A central hierarchical database that contains information that windows continually references during operation, such as profiles for each user, the applications installed on the computer and the types of documents that each can create, property sheet settings for folders and application icons, what hardware exists on the system and the ports that are being used.

# Windows Event Logs
Types of Logs:
	System Logs - Events logged by the operation system
	Application Logs - Events logged by third-party applications on the system
	Security Logs - Events logged by the system related to it's security

Window event logs are stored at C:\Windows\system32\winevt\logs as .evtx files

The EVTX files are in a binary format and require a special application to view the content. One built in program is Windows Event Viewer.

# Navigating Event Viewer

Event Type
	1. Error - Indicates a loss in data
	2. Warning - An event that indicates possible future issues
	3. Information - An event that indicates a successfully completed task
	4. Audit Success - An event that indicates a successfully audited security event 
	5. Audit Failure - An event that indicates a failed audited security event
Most common event types for each log category 
	System logs - Error, Warning, Information
	Application Logs - Error, Warning, Information 
	Security Logs - Audit Success, Audit Failure 

# Windows Registry

Windows Registry Components 
	Hives - A logical group of keys and values stored in disk files at C:\Windows\System32\Config
	Keys - Contains subkeys or values
	Values - stored data/configurations 