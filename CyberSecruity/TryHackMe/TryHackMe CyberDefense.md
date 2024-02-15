
	Enumerating SMB
		Enumeration is the process of gathering information on a target in order to find potential attack vectors and aid in exploration. The process is essential for an attack to be successful, as wasting time with exploits that either don't work or can crash the system can be a waste of energy. 
	SMB
		SMB share drives on a server that can be connected to and used to view or transer files. SMB can often be a great starting point for an attacker looking to discover sensitive information.
	Port Scanning
		The first step of enumeration is to conduct a port scan, to find out as much information as you can about the services, applications, structure and operating systm of the target machine. Nmap can be used for this.
	Enum4Linux
		Enum4Linux is a tool used to enumerate SMB shares on both windows and linux systems. It is bascially a wrapper around the tools in the Samaba package and makes it easy to quickly extract information from the target pertaining to SMB. It's installed by default on Parrot and Kali, however if you need to install it, you can do so from the offcial github.
		The syntax is easy starting at enum4linux [options] ip
		-u get userlist
		-m get machine list
		-n get namelist dump
		-s get sharelist
		-p get password policy information
		-g get group and member list