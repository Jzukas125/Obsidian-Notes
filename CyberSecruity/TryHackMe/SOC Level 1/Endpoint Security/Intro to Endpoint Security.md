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

# Sysinternals

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

# TCP view
	