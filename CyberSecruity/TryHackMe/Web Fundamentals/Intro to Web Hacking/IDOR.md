Learn how to find and exploit IDOR vulnerabilities in a web application, giving you access to data that you shouldn't have 

<h3> What is IDOR </h3>
IDOR stands for Insecure Direct Object Reference and is a type of access control vulnerability. This type of vulnerability can occur when a web server receives user-supplied input to retrieve objects, too much trust has been placed on the input data, and it is not validated on the server-side to confirm the requested object belongs to the user requesting it.

<h3> Finding IDORS in Encoded IDs </h3>
Most websites are encoded in base64 and can be decoded with cyberchef or another online tool, or the linux kernal itself.

<h3> Finding IDORS in Hashed IDs </h3>
Some hashes can be md5 and hashes are usually much longer than the original unhashed value.

<h3> Finding IDORs in Unpredictable IDs </h3>
If IDORs are not found using the above methods, two accounts could be created and then the ID's could be swaped between them. 

<h3> Where are IDORs </h3>
The vulnerable endpoint you're targeting may not always be something you see in the address bar. It could be content your browser loads in via an AJAX request or something that you find referenced in a JavaScript file.