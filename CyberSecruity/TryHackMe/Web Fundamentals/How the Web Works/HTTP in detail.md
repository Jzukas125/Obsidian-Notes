>	What is HTTPS
>HTTP - Hyper text transfer protocol is used whenever a website is viewed, and it is the set of ruled used for communicating with web servers for the transmission of webpage data, whether that is HTML, Images, Videos, etc.
>HTTPS - HTTPS is the secure version of HTTP. HTTPS data is encrypted, and it gives you the assurance that you're on the correct webpage unless it's some other type of connection such a tor connection.


>Requests are made to the web server for assets such as HTML, Images, and download the responses. Before the response is sent, the browser needs to be told specifically how to access the resources. 
>![[Pasted image 20230918233210.png]]
>Scheme: instructs on what the protocol for accessing the resource such as HTTP, HTTP and FTP. 
>User: Some services require authentication to log in, a username and password can be attached to the URL to log in.
>Host: Domain name or IP address of the server you wish to access
>Port: The port you're connecting to, usually 80 for HTTP and 443 for HTTPS
>Path: File name and location of the resource you are trying to access
>Query String: extra bits of information that can be sent to the requested path. For example, /blog?id=1 would tell the blog path that you wish to receive the blog article with the ID of 1
>Fragment: Reference to a location on the actual page requested. Commonly used for pages with long contact and can have page linked to it.


>	Making a request 
>Example
```
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/
```
>On line 1 the request is sending a GET method requesting a home page with / and telling the web server that HTTP protocol version 1.1 is being used. Then on line 2 we're telling the web server that we want the website tryhackme.com. On line 3 we tell the web server that we are using Firefox. Line 4 has us telling the server that [https://tryhackme.com](https://tryhackme.com/) is the web page that we are referring to. 


>HTTP methods are a way for the client to show their intended action when making an HTTP request. Here are the most common requests
>Get Request - used for getting information
>Post Request - Used for submitting data and potentially creating new records.
>Put Request - used for submitting data to a web server to update info
>Delete Request - deletes info


>	HTTP Status Codes
>The first line of an HTTP server response contains a status code informing the client of the outcome of their request and how to handle it. The status code can be broken down into 5 ranges:
>100-199 - Information Response -- Uncommon, tells the client that the code was accepted and that they should continue sending the rest of their request
>200-299 - Success -- range of codes to signifies the request was successful
>300-399 - Redirection -- redirects client's request to another resource can be a different webpage or website
>400-499 - Client Errors -- informs about errors
>500-599 - Server Errors --reserved for errors happening on the server-side, usually for a major problem with the server handling the request
>	Common HTTP Status Codes
>Common HTTP codes that you're likely to come across 
>200 - OK -- request was completed successfully
>201 - Created -- A resource has been created
>301 - Moved Permanently -- redirects client's browser to a new webpage or tells search engines that the page has moved elsewhere
>302 - Found -- similar to permanent redirect, but is only a temporary change and may change again
>400 - Bad request -- Something is either wrong or missing in the request
>401 - Not Authorized -- Currently not allowed to view the resource under their current perms 
>403 - Forbidden -- Do not have permission to view whether you're logged in or not
>405 - Method Not Allowed -- Resource does not allow this method request for example it expected a POST request, and you sent a GET request
>500 - Internal Service Error -- the service has encountered some kind of error with your request that it doesn't know how to handle properly 
>503 - Service Unavailable -- server is unable to handle your request because it's overloaded or down for maintenance


>	Headers
>Headers are additional bits of data that are sent to the web server when making requests. Headers are not required, but they do make viewing a website easier.
	Common Request Headers (headers that are sent from the client to the server)
	Host: Web servers host multiple websites and by providing the host headers you can tell it which one you need, or you will be given the default
	User-Agent: The browser software and version number, telling the web server your browser software helps it format the website properly by your browser and some elements of HTML, JavaScript and CSS.
	Content-Length: Tells the web server how much data to expect in the web request 
	Accept-Encoding: Tells the web server the type of compression method the browser supports, so the data can be made smaller
	Cookie: Data used to remember your information
		Common Response Headers 
	Set-Cookie: To store information that gets sent back to the web sever when requested
	Cache-Control: Determines the length of time for storing the content of a response in the browser's cache before it requests it again
	Content-Type: Tells the client what type of data is being returned 
	Content-Encoding: What method has been used to compress the data to make it smaller when sending it over the internet


>	Cookies
>When a Set-Cookie is used, cookies are saved to the browser and then every further request that is made, a cookie will be sent back to the web server. HTTP is stateless, meaning it doesn't track previous requests, cookies can be used to remind the web server who you are, personal settings, or if you've used the website before. 