I might not be taking many notes for this room as I do not care to do writeups.
To help me with this I will be referencing the snort cheat sheet that tryhackme created.
![[Snort cheat sheet PDF.pdf]]

I found this cheat sheet on https://cyvatar.ai/write-configure-snort-rules/
![[Pasted image 20240328160848.png]]
![[Pasted image 20240316165142.png]]
![[Pasted image 20240328170209.png]]


snort -c local.rules -A full -l . -r filename

<h3> Challenge 1: </h3>
Write rules to detect "all TCP port 80 traffic" packets in the given pcap file. 
What is the number of detected packets?
Answer: 164
I wrote 
```
alert tcp any 80 <> any any (msg:"TCP port 80 inbound traffic detected";sid:1000000000001; rev :1)
alert tcp any any <> any 80 (msg:"TCP port 80 outbound traffic detected";sid:1000000000002; rev :1)
```
into the local rules and then used 
snort -c local.rules -A full -l . -r mx-3.pcap
to look at its info

<h3> Challenge 2: </h3> 
Investigate the log file.  

What is the destination address of packet 63?

no rule is needed to find this packet as it in packet sniffing mode instead we use the command <br> snort -r snort.log.1712087408 -n 63
which we then look at the last packet to find its final IP address

<h3> Challenge 3: </h3>
