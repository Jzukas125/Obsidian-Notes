I might not be taking many notes for this room as I do not care to do writeups.
To help me with this I will be referencing the snort cheat sheet that tryhackme created.
![[Snort cheat sheet PDF.pdf]]

I found this cheat sheet on https://cyvatar.ai/write-configure-snort-rules/
![[Pasted image 20240328160848.png]]
![[Pasted image 20240316165142.png]]
![[Pasted image 20240328170209.png]]


snort -c local.rules -A full -l . -r filename

Challenge 1:
Write rules to detect "all TCP port 80 traffic" packets in the given pcap file. 
What is the number of detected packets?
Answer