My notes on the YouTube video [Beginner Bug Bounty Course | Web Application Hacking](https://www.youtube.com/watch?v=wMO_My5gsDI&list=PLtZtNPs3fJyDUJttw2sJVU69IKfqY7XPn)

# Recon and Tools

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
