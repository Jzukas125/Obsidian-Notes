>DNS - is Domain Name System that provides a simple way for us to communicate with devices on the internet without remembering complex numbers. Basically converts the IP address into a feasible name, such as 104.26.10.229 into tryhackme.com

>Domain Hierarchy 
>	TLD (Top-Level Domain) - The ending string of the website name, such as the .com on a website. Two types of TLD, gTLD (Generic Top Level) and ccTLD (Country Code Top Level Domain). gTLD is meant to tell the domain name's purpose, such as .gov for government. A ccTLD is used for geographical purposes, such as .ca for sites located in Canada.

>Second-Level Domain
>For example, tryhackme.com is a domain while the tryhackme is the second level domain. The second level domain is limited to 63 characters + the TLD and can only use an a-z 0-9

>Subdomain - sits on the left-hand side of the Second-Level Domain, using a period to separate it. For example, if you had a website called admin.tryhackme.com the admin part is the subdomain. The total length must be kept to 253 characters or less.

>DNS record types 
>	A record - these records resolve to IPv4 addresses, for example 104.26.10.229
>	AAAA record - records resolve to IPv6 addresses, i.e. 2606:4700:20::681a:be5
>	CHAME Record - these records resolve to another domain name i.e. TryHackMe's online shop has the subdomain name store.tryhackme.com which returns a CNAME record shops.shopify.com. Another DNS request would then be made to shops.shopify.com to work out the IP address
>	MX record - These resolve to the address of the server's email address, i.e. an MX record response for tryhackme.com would be alt1.aspmx.l.google.com. These also come with a priority flag. Good for when the main server goes down and email needs to be sent to the backup server.
>	TXT record - free text fields where any text-based data can be stored. TXT records common uses include listing servers that have authority to send an email on behalf of the domain.

>What happens when you make a DNS request 
>	1. When a domain name is requested, your computer checks its local cache to see if you've already looked up the address recently, if not a request to your recursive DNS server will be made.
>	2. A recursive DNS server is provided by your ISP, but you can choose your own. This server also has a local cache of recently looked up domain names. If a result is found locally, it's send back to your computer and the request ends. If it can't be found locally, then a journey begins to find the correct answer, starting with the internet's DNS servers.
>	3. The root server is the backbone of the internet, its job is to redirect you to the correct Top Level Domain Server, depending on the request. I.e. if you request www.tryhackme.com, the root server will recognize the Top Level Domain of .com and refer you to the correct TLD server that deals with the .com address. 
>	4. The TLD server holds records for where to find the authoritative server to answer the DNS request. The authoritative server is often also  known as the nameserver for the domain. For example, the name server for tryhackme is kip.ns.cloudflare.com.
>	5. An authoritative DNS server is the server that is responsible for storing the DNS records for a particular domain name and where any updates to your domain name DNS records would be made. DNS records all come with a TTL (Time to live) value.
>	6. ![[Pasted image 20230918170051.png]] Reference Image
>Answer the questions below
	What field specifies how long a DNS record should be cached for?  
	TTL
	What type of DNS Server is usually provided by your ISP?  
	Recursive
	What type of server holds all the records for a domain?
	Authoritative

>Task 5 Practical 
>The website used is just a terminal that emulates the nslookup command.
>What is the CNAME of shop.website.thm?
>(I used the nslookup --type=CNAME shop.website.thm) shops.myshopify.com
>What is the value of the TXT record of website.thm?
>THM{7012BBA60997F35A9516C2E16D2944FF}
>What is the numerical priority value for the MX record?
>30
>What is the IP address for the A record of www.website.thm?