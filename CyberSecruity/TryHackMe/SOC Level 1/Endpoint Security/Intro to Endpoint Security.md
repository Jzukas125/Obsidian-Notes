#TryHackMe 
# Room Introduction
The fundamentals of endpoint security monitoring, essential tools, and high-level methodology will be introduced. Some of the topics discussed will be Endpoint Security Fundamentals, Endpoint logging and monitoring, and Endpoint Log Analysis. 

# Endpoint Security Fundamentals

Core Windows Processes
	Information about core windows processes can be found using task manager. Task manager is a built-in GUI-based Windows utility that allows users to see what is running on the system

Task provides some of the core windows processes running in the background such as:
- System
- System > smss.exe
- csrss.exe
- wininit.exe 
- wininit.exe > services.exe
- wininit.exe > services.exe > svchost.exe
- lsass.exe
- winlogon.exe
- explorer.exe

<h3> Sysinternals </h3>
With the prior knowledge of Core windows processes, we can now proceed to discuss the available toolset for analyzing running artifacts in the backend of a windows machine. The sysinternals tools are a compilation of over 70+ windows-based tools. Each of the tools falls into one of the following categories:
- File and Disk Utilities
- Networking Utilities
- Process Utilities
- Security Utilities
- System Information
- Miscellaneous

We will introduce two of the most used sysinternals tools for endpoint investigation for this task. 
- TCP view - Networking Utility tool
- Process Explorer - Process Utility tool 

<h3> TCP view </h3>
TCP view is a windows program that will show a detailed listings of all TCP and UDP endpoints on your system, including the local and remote addresses and state of TCP connections. On window server 2008, Vista, and XP, TCPView also reports the name of the process that owns the endpoint. TCPView provides a more informative and conveniently presented subset of the Netstat program that ships with Windows. The TCPView download includes Tcpvcon, a command-line version with the same functionality.

Process Explorer
Allows us to see 
- Associated services
- Invoked network traffic
- Handles such as files or directories opened
- DLLs and memory-mapped files loaded

# Endpoint Logging and Monitoring

Endpoint logging allows us to collect and aggregate them for searching capabilities, and better automate the detection of anomalies. 

<h3> Windows Event Logs </h3>
Windows event logs are not text files can be viewed using a text editor.  However the raw data can be translated into XML using the Windows API. The events in these log files are stored in proprietary binary format with a .evt or .evtx extension. The log files with .evtx file extension typically reside in C:\Windows\System32\winevt\Logs.

3 main ways of accessing event logs within a Windows system:
1. Event Viewer
2. Wevtutil.exe
3. Get-WinEvent

<h3> Sysmon </h3>
Sysmon is a tool used to monitor and log events on Windows, commonly used by enterprises as part of their monitoring and logging solutions. Sysmon is similar to windows event logs with further detail and granular control.

Gathers very detailed information, commonly used with a SIEM.

<h3> OSQuery </h3>
Open-source tool created by Facebook. Can query an endpoint using SQL syntax. Osquery can be installed on various platforms.

<h3> Wazuh </h3>
Wazuh is an open source, freely available, and extensive EDR solution, which security engineers can deploy in all scales of environments. 

# Endpoint Log Analysis 

<h3> Event Correlation </h3>
Each correlation identifies significant relationships from multiple log sources such as application logs, endpoint logs, and network logs. Event correlation deals with identifying significant artefacts co-existing from different log sources and connecting each related artefact. 

<h3> Baselining </h3>
Baselining is the process of knowing what is expected to be normal. In terms of endpoint security monitoring, it requires a vast amount of data gathering to establish the standard behavior of user activities, network traffic across infrastructure, and processes running on all machines owned by the organization. 