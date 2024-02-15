>	Putting it All together
>time to use your pea sized brain and put everything together.
>To put into summary, when a website is requested, your computer needs to know the server's IP address it needs to talk to; for this is uses DNS. Your computer talks to the web server using a special set of commands called the HTTP protocol; the web server then returns HTML, JavaScript, CSS, Images, etc., which your browser then uses to correctly format and display the website to you


>	Load Balancers
>When a website's traffic starts getting too large or is running an application that needs high availability, one web server might no longer do the job. Load balancers provide two main features, which are ensuring high traffic websites can handle the load and providing a failover if a server becomes unresponsive. When a website is requested with a load balancer, the load balancer will receive your request first and then forward it to one of the multiple servers behind it. The load balancer uses different algorithms to determine the server is best toe deal with the request. A couple of examples of these algorithms are round-robin, which sends it to each server in turn, or weighted, which checks how many requests a server is currently dealing with and sends it to the least busy server.
>Load balancers also perform periodic checks with each server to ensure they are running correctly; this is called a health check. If a server doesn't respond appropriately or doesn't respond, the load balancer will stop sending traffic until it responds appropriately again. 
>- CDN (Content Delivery Networks) - A CDN can be an excellent resource for cutting down traffic to a busy website. It allows you to host static files from your website, such a JavaScript, CSS, Images, Videos, and host them across thousands of servers all over the world. When a user requests a hosted file, the CDN decides where the nearest server is physically located and sends the request there instead of potentially the other side of the world. 
>- Databases - Websites communicate with databases to store and recall data. Databases can be either from a simple plain text file up to complex clusters of multiple servers, providing speed and resilience. 
>- WAF (Web Application Firewall) - A WAF sits between your web request and the web server; its main purpose is to protect the web server from hacking or denial-of-service attacks. It analyses the web requests for common attack techniques, whether the request is from a real browser rather than a bot. It also uses rate limiting which checks if an excessive amount of web requests and only allows a certain amount of requests from an IP per second. If a request is deemed a potential attack, it will be dropped and never sent to the web server.


>	How Web servers work.
>What is a Web Server?
>A web server is a software that listens for incoming connections and then utilizes the HTTP protocol to deliver web content to its clients. The most common web server software you'll come across is Apache, Nginx, IIS and Node.js. A web server delivers files from the root directory, which is defined in the software settings. 
>For example, Nginx and Apache share the same default location of /var/www/html in Linux operating systems, and IIS uses C:\inetpub\wwwroot for the windows operating systems. If you requested the file http://www.example.com/picture.jpg it would send the file /var/www/html/picture.jpg from its local hard drive.
>Virtual Hosts
>Web servers can host multiple websites with different domain names; to achieve this, a virtual host is used. The web server software checks the hostname being requested from the HTTP headers and matches that against its virtual hosts. If it finds a match, the correct website will be provided. If no match is found, the default website will be provided instead.
>Virtual Hosts can have their root directory mapped to different locations on the hard drive. For example, one.com being mapped to /var/www/website_one, and two.com being mapped /var/www/website_two. There's no limit to the number of different websites you can host on a web server.
>Static Vs Dynamic Content
>Static content is content that never changes. Common examples of this are pictures, JavaScript, CSS etc. but can also include HTML that never changes. Furthermore, there are files that are directly served from the web server with no changes made to them. 
>Dynamic content is content that could change with different requests, which include something like a blog. On the homepage it would show the latest entries, if a new entry is created, then the home page is updated with the latest entry, or a second example might be a search page on a blog. Depending on what is searched, different results will be displayed. The changes done are in the backend with the use of programming languages. HTML source is unable to be viewed and see what's happening in the backend, while the HTML is the result of the processing from the Backend. Everything that's visible is the frontend.
>	Scripting and Backend Languages
>There's no limit to what backend can do, and these are what a website interactive to the user. An example of the languages are PHP, Python, Ruby, Node.js, Perl, and many more. The languages can interact with databases, call external services, process data from the user, and much more. 
>An example of a PHP request includes
>`<html><body>Hello <?php echo $_GET["name"]; ?></body></html>`
>Which it then outputs 
>`<html><body>Hello adam</body></html>`
>The PHP doesn't show when request because it is in the Backend. This level of interactivity opens up a lot more security issues for web apps that haven't been created securely.