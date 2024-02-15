>	Firstly, we should ask, in the context of web application security, what is content? Content can be files, videos, pictures, backup and a website feature. When talking about content discovery, we're not talking about obvious things such as things viewed on a website; it's the things that aren't immediately presented to us and that weren't always intended for public access. This content could be pages or portals intended for staff usage, older versions of the website, backup files, configuration files, administration panels, etc. There are three main ways of discovering content on a website, which include: Manually, Automated and OSINT.

>	Manual Discovery - Robots.txt
>There are manually places that can be manually checked on a website to start discovering more content. 
>The robots.txt file is a document that tells search engines which pages they are and aren't allowed to shoe on their search engine results or ban specific search engines from crawling the website altogether. It's common practice to restrict certain website areas, so they aren't displayed in search engine results. These pages may be areas such as administration portals or files meant for the website's customers. This file gives us a great list of locations on the website that the owners don't want us to discover as penetration testers. 


>	Favicon
>The favicon is a small icon displayed in the browser's address bar or tab used for branding a website.  Sometimes when frameworks are used to build websites, a favicon that is part of the installation gets leftover, and if the website developer doesn't replace this with a custom one, this can give us a clue on what framework is in use. OWASP hosts a database of common framework icons that can be used to check target favicons, https://wiki.owasp.org/index.php/OWASP_favicon_database. Once the framework stack is known, external resources can be used to discover more about it. 
>We were given a task to find the framework of a website using the favicon. I simply downloaded the image by using the curl function with the website URL and piped md5sum (`curl https://static-labs.tryhackme.cloud/sites/favicon/ | md5sum`). Using the md5 hash I check the favicon wiki and searched for the framework used which is cgiirc.


>	Manual Discovery - Sitemap.xml
>Unlike the robots.txt file, which restricts what search engine crawlers can look at, the site map.xml file gives a list of every file the website owner wishes to be listed on a search engine. These can sometimes contain areas of the website that are a bit more difficult to navigate to, or even list some old webpages that the current site doesn't use anymore but are still there.


>	Manual Discovery - HTTP Headers
>When requests are made to a web server, the server returns various HTTP headers. These headers can contain useful information such as the web server software and possibly the programming/scripting language being used. Can be accessed by using the curl command and the HTTPS URL to the website and a -v (curl http://10.10.159.204 -v)


>	Manual Discovery - Framework Stack
>Once the framework is found by either the favicon or by looking in the page source comments, copyright notices or credits, we can then learn more about the software and other information, potential allowing even more content to be discovered. 
>To answer the question I went on the framework website and found the framework link and pasted it on the end of the acme it support website. That then lead to a login page with a username and password input. Luckily they have not changed from the default credentials with the username and password being admin. 


>	OSINT - Google Hacking / Dorking
>There are also external resources available that can help in discovering information about your target website; these resources are often referred to as OSINT or as they're freely available tools that collect information. 
>	Google Hacking/Dorking 
>Google dorking allows us to pick out custom content with custom domains such as using the site:filter for example (site:tryhackme.com) you can then use this to match this with the certain search terms such as the word admin (site:tryhackme.com admin) this would only return results from the tryhackme.com website which contains the word admin in its content. You can combine multiple filters as well, of which include:
>site - site:tryhackme.com -- returns results only from the specified website address
>inurl - inurl:admin -- returns results that have the specified word in the URL 
>filetype - filetype:pdf -- returns results which are a particular file extension
>intitle - intitle:admin -- return results that contain the specified in the title 


>	OSINT - Wappalyzer 
>Wappalyzer is an online tool and browser extension that help identify what technologies a website uses, such as frameworks, Content Management Systems (CMS), payment processors and much more, and it can even find version numbers as well.


>	OSINT - Wayback Machine 
>The Wayback Machine is a historical archive of websites that dates back to the late 90s. Domain names can be searched, and it'll show all the times that service scraped the web page and saved the contents. This can help uncover old pages that may still be active on the current website.


>	OSINT - GitHub
>To understand GitHub, an understanding of Git must be established. Git is a version control system that tracks changes to files in a project. It makes working in a team easier due to its saving process. When changes are made, they need to be committed and then pushed to a repository. GitHub is a hosted version of Git on the interwebs. Repositories can either be set to public or private and have various access controls. Many companies GitHub accounts can be found and once discovered you might be able to access source code, passwords or other content that hadn't been found yet.


>	OSINT - S3 buckets
>S3 Buckets are a storage service provided by AWS which allows people to save files and even static website content in the cloud, accessible over HTTP and HTTPS. The owner of the files can set access permissions to either make files public, private and even writable. Sometimes the access permissions are incorrectly set and inadvertently allow access to files that shouldn't be available to the public. The format of the S3 bucket is http(s)://{name}.s3.amazonaws.com where {name} is decided by the owner, such as tryhackme-assets.s3.amazonaws.com. S3 buckets can be discovered in many ways, such as finding the URL's in the website's page source, GitHub repositories, or even automating the process. One common automation method is by using the company name followed by common terms such as {name}-assets, {name}-www, {name}-public, {name}-private, etc


>	Automated Discovery 
>Automated discovery is the process of using tools to discover content rather than doing it manually. This process is automated as it usually contains hundreds, thousands or even millions of requests to a web server. These requests check if a file exists on a website, giving us access to resources we didn't previously know existed. 
>	Word lists
>Word lists are text files that contain a long list of commonly used words that can be used in several different cases. For example, a password word list would include the most frequently used passwords, where we're looking for content in our case, so we'd require a list containing the most commonly used directory and file names. An excellent source of this is https://github.com/danielmiessler/SecLists.

>	Automation Tools
>Three content discovery tools that we'll be going over is  ffuf, dirb, and gobuster.
>