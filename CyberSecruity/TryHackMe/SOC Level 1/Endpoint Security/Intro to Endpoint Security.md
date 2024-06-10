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
Windows event logs are not text files can be viewed using a text editor.  However the raw data can be translated into XML using the Windows API. The events in these log files are stored in proprietary binary format with a .evt or .evtx extension. The log files with .evtx file extension typi