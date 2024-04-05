#CCDC 
Nmap stands for network map. Nmap is a port scan that sends a probe to each port on a system and returns data based on its status. Nmap can be force probed. Nmap can be run in tandem with the ping command.

The ping command will find the IP address of the thing pinged such as google.com
***You do not need an ip to nmap a website***

```
ping google.com
```

You can run nmap on local host to receive information and looks like 
```
nmap localhost
```
Starting Nmap 7.93 ( https://nmap.org ) at 2024-02-21 19:44 EST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00024s latency).
Other addresses for localhost (not scanned): ::1
Not shown: 998 closed tcp ports (conn-refused)
PORT    STATE SERVICE
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds

Nmap done: 1 IP address (1 host up) scanned in 0.10 seconds


```
nmap -Pn localhost
```
This command allows you to see extra ports that won't show up on a regular scan


```
namp -sV localhost
```
This command does version detection 

```
nmap --traceroute localhost
```
This command traces a route that a packet would take to travel across the network

```
nmap -A localhost
```
-A performs everything which is -Pn and traceroute plus more that I can not name right now

