My notes on the YouTube video [Beginner Bug Bounty Course | Web Application Hacking](https://www.youtube.com/watch?v=wMO_My5gsDI&list=PLtZtNPs3fJyDUJttw2sJVU69IKfqY7XPn)

# Recon and Tools

![[Pasted image 20240322154102.png]]
Basic starting guide I found on [GitHub](https://github.com/m0chan/BugBounty/tree/master) that should be easy enough to follow

To start it is important that we have any note taking method to make sure we do not continually run through the same processes in a web page. Something similar to a playbook could be helpful.

First tool being installed is gedit. This will be to edit files with something other than Nano or vim.
	Very similar to notepad, just is in Linux.

<h3> Sublist3r </h3>
Sublist3r is an important tool for finding subdomains in a website and is important for starting recon.

Usage
```
sublist3r -d google.com
```
This command is a simple one as it only really has one addition. We type sublist3r to simply start using the command, and then type -d to specify we're typing a websites domain and then the domain of the website we want to search.

This is usually a starting point to go from as we can now brute force endpoints with.

<h3> ffuf </h3>
ffuff is a fast web fuzzer that allows typical directory discovery, virtual host discovery and GET and POST parameter fuzzing. This is especially useful for pentesters, ethical hackers, and forensics experts because  it allows for the discovery of hidden files, directories or subdomains.

Type 
```
ffuf -help
```
to learn about ffuf

Ffuf requires a wordlist in order to function
```
ffuf -w /usr/share/wordlists/example.txt -u https://www.yahoo.com/FUZZ -fl 1
```

I had to have chatgpt explain this due to me not having full understanding of how to use ffuf.
- `-w /usr/share/wordlists/example.txt`: This flag specifies the wordlist (dictionary) to be used for fuzzing. In this case, you're using a wordlist located at `/usr/share/wordlists/example.txt`. Wordlists contain a list of words that will be used to replace the `FUZZ` placeholder in the URL.

- `-u https://www.yahoo.com/FUZZ`: This flag specifies the target URL to fuzz. `FUZZ` acts as a placeholder that will be replaced by each word from the wordlist during the fuzzing process. So, `ffuf` will send requests to URLs like `https://www.yahoo.com/word1`, `https://www.yahoo.com/word2`, and so on, using the words from the wordlist.

- `-fl 1`: This flag specifies the filtering level. In this case, it's set to `1`, meaning that responses with HTTP status codes less than or equal to 1xx (informational responses) will be considered valid. This helps in filtering out unwanted responses.

<h3> dirb </h3>
The official definition of dirb from the kali website is "DIRB is a Web Content Scanner. It looks for existing (and/or hidden) Web Objects. It basically works by launching a dictionary based attack against a web server and analyzing the responses.

DIRB comes with a set of preconfigured attack wordlists for easy usage but you can use your custom wordlists. Also DIRB sometimes can be used as a classic CGI scanner, but remember that it is a content scanner not a vulnerability scanner.

DIRB’s main purpose is to help in professional web application auditing. Specially in security related testing. It covers some holes not covered by classic web vulnerability scanners. DIRB looks for specific web objects that other generic CGI scanners can’t look for. It doesn’t search vulnerabilities nor does it look for web contents that can be vulnerable." 

You can simply type 
```
dirb https://yahoo.com
```
to test for any hidden items that weren't found through any other means

<h3> Google Dorking </h3>
Google dorking is always a good tool to use for finding new information. More information can be found [here](https://www.simplilearn.com/tutorials/cyber-security-tutorial/google-dorking)

<h3> Burp Suite </h3>
Burp Suite is incredibly important to use but requires a little bit more knowledge about it.
Need to change to your localhost proxy (127.0.0.1 port 8080) in order to access burp suite through the browser
I will be taking notes on TryHackMe's how to use burp suite soon.

<h3> VPN </h3>
Good idea to have a vpn in case your IP address gets banned from doing malicious requests and VPN will allow anybody to just retry and continue. 

<h3> Nmap </h3>
Nmap is an important tool for bug hunting because it allows to enumerate and find any open ports. More can be found in the [[Nmap]] section of notes.

# URL Testing
To start of course run dirb to find any sub urls, and then inspect the html source code.
Any hidden urls can be copy and pasted and attached to the end of the current URL.
Hacker101 CTF has a lot of practice resources to help learn how to fully analyze a site.