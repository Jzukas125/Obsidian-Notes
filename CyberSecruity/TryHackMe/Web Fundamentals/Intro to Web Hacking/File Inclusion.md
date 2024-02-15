<h3> Intro </h3>
This rooms aims to equip us with basic knowledge to exploit file inclusion vulnerabilities, including Local File Inclusion, Remote File Inclusion, and directory traversal. 
In some scenarios web applications are written to request access to files on a given system, including images, static test, and so on. ![[Pasted image 20231203235523.png]]

For example, parameters are used with Google searching, where GET requests pass user input into the search engine.  Let's say a user sends an HTTP request to the webserver that includes a file to display. For example, if a user wants to access and display their CV within the web application, the request may look as follows, http://webapp.thm/get.php?file=userCV.pdf, where the file is the parameter and the userCV.pdf, is the required file to access.

<h3> Why do these happen </h3>
FIV are commonly exploited in various programming languages for web applications such as PHP that are poorly written and implemented. The main issue is the input validation of which can happen when the inputs are not sanitized or validated and the user controls them.  

<h3> Risk </h3>
Attacker can leverage file inclusion vulnerabilities to leak data such as code, or other important information related to the web application or operating system. Files that can be written into any server can be used to gain remote command execution. 


# Path Traversal
Also known as directory traversal, a web security vulnerability allows an attacker to read operating system resources, such as local files on the server running an application. The attacker exploits this vulnerability by manipulating the web application's URL to locate and access files or directories stored outside the application's root directory. 
Path traversal vulnerabilities occur when the user's input is passed to a function such as file_get_contents in PHP. Often poor input validation or filtering is the cause of the vulnerability. In PHP, you can use file_get_contents to read the content of a file.

# Local File Inclusion
LFI attacks are often due to stupid developers that lack security awareness. With PHP, using functions such as include, require, include_once, and require_once often contribute to vulnerable web applications. We'll be using PHP as an example, but LFI vulnerabilities also occur when using languages such as ASP, JSP, or even node.js. LFS exploits follow the same concept as path traversal. 
 Answers for the CTF's 

Lab3
lab3.php?file=../../../../etc/passwd%00

Lab4
/lab4.php?file=../../../etc/passwd/

 lab 5
 lab5.php?file=....//....//....//....//etc/passwd

Lab 6

lab6.php?file=THM-profile/../../../../../etc/passwd

lab6.php?file=THM-profile/../../../../../etc/os-release

# Remote File Inclusion - RFI 
RFI is a technique to include remote files and into a vulnerable application. Similar to LFI, the RFI occurs when improperly sanitizing user input, allowing an attack to inject an external URL into include functions. One requirement for RFI is that the allow_url_fopen option needs to be on. 
RFI has a higher risk than LFI, since RFI vulnerabilities allow an attack to gain Remote Command Execution (RCE) on the server. Examples include Sensitive Information Disclosure, Cross-sire Scripting, Denial of Service. An external server must communicate with the application server for a successful RFI attack, where the attacker hosts malicious files on their server. 

