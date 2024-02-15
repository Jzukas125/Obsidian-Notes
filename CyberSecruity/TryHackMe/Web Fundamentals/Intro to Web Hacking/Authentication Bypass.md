>	Brief
>In this room I'll learn about different ways website authentication methods can be bypassed, defeated or broken. These vulnerabilities can be crucial when it comes to info leaks

>	Username Enumeration
>Username enumeration is a common application vulnerability which occurs when an attack can determine if usernames are valid or not, usually used in a brute force manner. Creating a list of usernames is a helpful way to start, and we can start doing this with website error messages. If you try filling in information on the ACME IT Support website, it will give us an error saying that the username already exists. We can produce a list of usernames using this info by using the ffuf tool. (The URL for the website is dynamic and changes per machine)
>`ffuf -w /usr/share/wordlists/SecLists/Usernames/Names/names.txt -X POST -d "username=FUZZ&email=x&password=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u http://10.10.16.161/customers/signup -mr "username already exists"
>-w argument selects the file's location on the computer that contains the list of usernames that we're going to check
>-x argument specifies the request method, this will be a GET request by default
>-d specifies the data being sent
>In the example, we have the fields username, email, password, and cpassword. We've set the value of the username to FUZZ. In the ffuf tool, the FUZZ keyword signifies where the contents from our wordlist will be inserted in the request. 
>-H is used for adding additional headers to the request
>Content-Type was set to the webserver knows we are sending form data.
>-u specifies the URL we are making a request to
>-mr is the text on the page we are looking for to validate we've found a valid username

>	Brute Force
>Using the previous file, we can now attempt a brute force attack on the login page. 
>`ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://10.10.54.42/customers/login -fc 200`
>The ffuf keyword will be used again, and instead of using FUZZ to select where in the request the data from the wordlists will be inserted, but because we're using multiple wordlists, we have to specify our own FUZZ keyword. In this instance, we've chosen W1 for the list of valid usernames and W2 

>	Logic Flaw
>A logic flaw is when the typical logical path of an application is either bypassed, circumvented or manipulated by a hacker. Logic flaws can exist anywhere in a website.
>	Example
>`if( url.substr(0,6) === '/admin') {
    # Code to check user is an admin
} else {
    # View Page
}`
 The code above checks to see whether the start of the path the client is visiting begins with /admin and if so, then further checks are made to see if the client is an admin. If the page doesn't begin with /admin the page is shown to the client. Because the above code uses three equals signs, it's looking for an exact match on the string, including the same letter casing. The code presents a logic flaw by allowing an unauthenticated user requesting /adMin will not have their privileges checked and have the page displayed to them, bypassing the authentication checks.


> Cookie Tampering
> 	Editing cookies can grant elevated privileges
> 	Cookies can come in pain text, making obvious of their purpose. 
> 	Take, for example, if these were the cookie set after a successful login:
> 	Set-Cookie: logged_in=true; Max-Age=3600; Path=/
> 	Set-Cookie: admin=false; Max-Age=3600; Path=/
> 	We see that one cookie appears to control whether the user is logged in or not, and another controls whether the visitor has admin privileges (admin).
> 	Encoding in linux can be done by typing "echo 'thing i want to encode' | 'language i want it to be decoded from' -d"
> 	Same goes with encoding but remove the -d