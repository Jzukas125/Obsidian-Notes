>	Brief
>Subdomain enumeration is the process of finding valid subdomains in order to expand our attack surface and try to discover more potential points of vulnerability. The three types of subdomain enumeration that will be covered are brute force, osint, and virtual host.

>	OSINT - SSL/TLS Certificates
>when an SSL/TLS certificate is created for a domain by a CA, CA's take part in what's called "Certificate Transparency (CT) logs". These are publicly accessible logs of every SSL/TLS certificate created for a domain name. The purpose of Certificate Transparency logs is to stop malicious and accidental certificates from being used. We can use this service to our advantage to discover subdomains belonging to a domain, sites like http://crt.sh/ offer a searchable database of certificates that shows current and historical results.

>	OSINT - Search Engines
>Search engines contain trillions of links to more than a billion websites, which can be an excellent resource for finding new subdomains. Using advanced search methods on websites like Google, such as the site: filter, can narrow the search results. For example, "-site:www.domain.com.site:*.domain.com" would only contain results leading to the domain name domain.com but exclude any links to www.domain.com; therefore, it shows us only subdomain names belonging to domain.com. 

>	DNS Brute force
>Brute force DNS enumeration is the method of trying many different possible subdomains from a pre-defined list of commonly used subdomains. Because this method requires many requests, we automate it with tools to make the process quicker. In this instance, we are using a tool called dnsrecon to perform this.

>	OSINT - Sublist3r
>Automation using Sublist3r: helps speed up the process of OSINT subdomain discovery, we can automate the above methods with the help of tools like Sublist3r simulation to discover a new subdomain.

>	Virtual Hosts 
>Some subdomains aren't always hosted in publicly accessible DNS results, such as development versions of a web application or administration portals. Instead, the DNS record could be kept on a private DNS server or recorded in the developer's machine in their etc file. 
>Because web servers can host multiple websites from one server when a website is requested from a client, the server knows which website that client wants from the Host header. We can utilize the host header by making changes to it and monitoring the response to see if we've discovered a new website. Similar to DNS brute force, the process can be automated by using a wordlist. 