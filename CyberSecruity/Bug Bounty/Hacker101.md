<h3> Must-Have Tools </h3>
Burp Proxy but free works fine
	Allows us to watch all HTTP(S) communications, intercept and modify requests, and replay existing requests

Firefox
	Allows anyone to set proxy settings specifically in the browser, rather than setting them system-wide

Breaker mindset
	Here to break things before anyone else can, so that vulnerabilities can be fixed before actual attackers can get to them and in order to do so we need to understand how attackers operate, what their goals are, and how they think
	Need to understand what an application is doing and why it's doing it
	Attackers will always have an advantage over defenders

Attacker Goals 	
	When assessing an application, find every bit of functionality. Once you have a rough list of all the bits try to find an attacking goal. For example say you want credit card numbers from an e-commerce site; maybe I'd want to destroy or falsify data in a server monitoring application 

Prioritization 
	Need to rank areas of the application in terms of payoff: if I compromise area X, does that give me low-value or high-value information? What if I did Y? 
	When possible asking developers "What keeps you up at night?" will often point to areas to check

Findings 
	Reports should be as follows
	Title -- E.g. "Reflected Cross-Site Scripting in profiles"
	Severity 
	Description -- Brief description of what the vulnerability is 
	Reproduction Steps -- Brief description of how to reproduce the bug; preferably with a small proof of concept 
	Impact -- What can be done with the vulnerability?
	Mitigation -- How is it fixed?
	Affected assets -- Generally a list of affected URLs

Severity
	Base it on difficulty of exploitation and potential business impact
	Informational - Issue has no real impact
	Low - The business impact is minimal
	Medium - Potential to cause harm to users, but not revealing data
	High - Potential to reveal user data or aids in exploitation of other vulnerabilities 
	Critical - High risk of personal/confidential data exposure, general system compromise, and other severe impacts to the business.

HTTP Requests 
	Basic format as follows:
``` html
		VERB /resource/locater HTTP/1.1
		Header1: Value1
		Header2: Value 2
		...
		<Body of request>
```

Request Headers
	Host: Indicates the desired host handling the request 
	Accept: Indicates what MIME type(s) are accepted by the client; often used to specify JSON or XML output for webservices
	Cookie: Passes cookie data to the server
	Referrer: Page loading to this request (not passed to other servers when using HTTPS on the origin)
	Authorization: Used for 'basic auth' pages (mainly). Takes the form "Basic <base64'd username:password>"

Cookies
	Key-value pairs of data that are sent from the server and reside on the client for a fixed period of time.
	Each cookie has a domain pattern that it applies to and they're passed with each request the client makes to matching hosts.

Cookie Security
	Cookies added for .example.com can be read by any subdomain of example.com
	Cookies added for a subdomain can only be read in that subdomain and its subdomains 
	A subdomain can set cookies for its own subdomains and parent, but it can't set cookies for sibling domains.
	E.g. test.example.com can't set cookies on test2.example.com, but can set them on example.com and foo.test.example.com
	Two important flags to know for cookies 
		Secure: The cookies will only be accessible to HTTPS pages
		HTTPOnly: The cookie cannot be read by JavaScript 

# HTML

Parsing 
	HTML should be parsed according to the relevant spec, generally HTML5 now
	Often not parsed by your browser but also Web-Application Firewalls and other filters.
	Whenever there's a discrepancy in how these two items parse things, there's probably a vulnerability 
	Example:
		You can go to https://example.com/vulnerable?name=<script/xss%20src=http://evilsite.com/my.js> and it generates
		![[Pasted image 20240325211333.png]]
		A bad XSS filter on the web application may not see that as a script tag due to it being a 'script/xss' tag. But Firefox's HTML parser, for instance, will treat the slash as whitespace, enabling the attack.
Legacy Parsing 
	Due to decades of bad HTML, browsers are quite excellent at cleaning up after authors, and these conditions are often exploitable 
	- '`<script>` tag on its own will automatically be closed at the end of the page