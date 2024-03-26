Notes on the video [Hacker101](https://www.youtube.com/watch?v=HGaFCcWM57U&list=PLxhvVyxYRviZd1oEA9nmnilY3PhVrt4nj&index=3)
# XSS Review

Three types of XSS that is going to be covered today:
	Reflected XSS - Input from a user is directly returned to the browser, permitting injection of arbitrary content 
	Stored XSS - Input from a user is stored on the server and returned later without proper escaping
	DOM XSS - Input from a user is inserted into the page's DOM without proper handling, enabling insertion of arbitrary nodes
Recognition 
	Should follow a mental checklist for each input 
	1. Figure out where it goes: Does it get embedded in a tag attribute? Does it get embedded into a string in a script tag?
	2. Figure out any special handling: Do URLs get turned into links like posts in level1?
	3. Figure out how any special characters are handled: A good way is to input something like '<>;:''
	From those three steps, you'll know whether or not a given input is vulnerable to XSS
	At this point, one of the differences between stored and reflected XSS becomes apparent: rXSS vulnerabilities to be exploitable, in the case of POSTs
	If your rXSS exists just in a GET, you're fine, but your dependent on CSRF otherwise 
Exploitation Case 1
	During the special character test, you notice that angle brackets are passed through without encoding, and your input is being shown in a text node of the document
	In that case, a simple payload like `<script>alert(1)</script>` will almost definitely work.
	In very rare cases, a WAF or other filtering may detect the script tag and prevent execution 
Exploitation Case 2
	A closely related variant of the first case is when your input is being reflected in a tag attribute
	In this case, your first priority is to break out of the attribute, but in most cases you don't need to leave the tag at all -- meaning no need for angle brackets
	In level1's posts, you may have noticed that URLs were automatically turned into links. So the post "Check out <a href="https://google.com">http://google.com<a>
	What you may have noticed is that the double quotes were passed through without encoding, despite that angle brackets were not.