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