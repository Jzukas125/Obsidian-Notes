Server-Side Request Forgery is a vulnerability that allows malicious users to cause the webserver to make an additional or edited HTTP request to the resource of the attacker's choosing. 
Two Types 
	Type one - Regular SSRF where data is returned to the attacker's screen
	Type two - Blind SSRF vulnerability where an SSRF occurs, but no information is returned to the attacker's screen
A successful attack can result in access to unauthorized areas, access to customer/organizational data, ability to scale to internal networks, and reveal authentication tokens/credentials 

# Finding an SSRF
Potential SSRF vulnerabilities can be spotted in web applications in many different ways. Common examples 
![[Pasted image 20240118194924.png]]

Some are easier to exploit than others and usually trial and error is the best method

If working with a blind SSRF where no output is reflected, an external HTTP logging tool to monitor requests such as requstbin.com, your own HTTP server or Burp Suite's Collaborator client should be used. 

# Defeating Common SSRF Defenses
There are usually SSRF checks to make sure requested resources meet specific rules. There are usually two approaches, of which is either a deny list or an allow list.
<h3> Deny List </h3>
A deny list is where all requests are accepted apart from resources specified in a list of matching a particular pattern.  This may be implemented to protect sensitive endpoints, IP addresses or domains from being accessed by the public while still allowing access to other locations. A specific end point to deny is the localhost which may contain server performance or sensitive information. A deny list can by bypassed by using alternative localhosts such as 0, 0000, 127.1, or subdomains that have DNS record which resolves to the IP address 127.0.0.1 such as 127.0.0.1.nip.io. 

<h3> Allow list </h3>
An allow list is where all requests get denied unless that appear on a list or match a particular pattern, such that an URL used in a parameter must begin with "https://website.thm". An attacker could quickly circumvent this rule by creating a subdomain on an attacker's domain name, such as "https://webstie.thm.attackers-domain.thm". This application logic would now allow input and let an attacker control the internal HTTP request.

<h3> Open Redirect </h3>
Open redirect is an endpoint on the server where the website visitor gets automatically redirected to another website address. Take, for example, the link https://website.thm/link?url=https://tryhackme.com. This endpoint was made to record clicks for marketing but imagine if there was a potential SSRF vulnerability with stringent rules which only allowed URLs beginning with https://website.thm/. An attacker could use this feature to redirect internal HTTP requests to a domain of their choice 

# SSRF Practical 
We've come across two new endpoints during a content discovery exercise against the **Acme IT Support** website. The first one is **/private**, which gives us an error message explaining that the contents cannot be viewed from our IP address. The second is a new version of the customer account page at **/customers/new-account-page** with a new feature allowing customers to choose an avatar for their account.

I begin by opening my VM in tryhackme and then accessing the website. Then I need to create a customer account and log in. After that, I need to navigate to the avatar selection page, by viewing the page source of the avatar form, I can see the avatar form field value that contains the path to the image. I then inspect a new avatar that I choose to update to and I change its value to private to see if it will allow anything. Unfortunately, the website has a deny list and blocks access to the /private endpoint. Luckily, we can bypass this by writing x/../private (this works because the server knows that the ../ sting means to move up a directory and that now translates the request to just private). This works as the avatar updates into nothing, but if we inspect it, we can see a string of base 64 is output in the div class. Once decoded, we get the flag and complete the challenge.