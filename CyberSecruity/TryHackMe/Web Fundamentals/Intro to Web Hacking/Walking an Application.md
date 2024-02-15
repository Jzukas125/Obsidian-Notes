>	Walking an Application <b> Go back to this page when starting </b>
>In this room, I will learn how to manually review a web application for security issues using only the built-in tools in my browser. More often than not, automated security tools and scripts will miss many potential vulnerabilities and useful information
>The tools I will learn and use are:
>View Source: Using the browser to view the human-readable source code of a website
>Inspector: Learn how to inspect elements and change blocked content to be viewed
>Debugger: Inspect and control the flow of a page's JS
>Network: see the network requests a page makes


>	Exploring the Website
>As a future pen tester, my job would be to review a website and discover features that could potentially be vulnerable and attempt to exploit them to assess whether they are. These features are usually parts of the website that require some interactivity with the user. Finding interactive portions of the website can be as easy as spotting a login form to manually reviewing the website's JavaScript. 
>A good example is to use the website that was given to us by the room and to start looking around are specific locations such as:
>Home Page - URL / -- Contains a summary of what ACME IT Support does with a company photo of their staff
>Latest News - URL /news -- Contains a list of recently published news articles by the company, and each news article has a link with an ID number, i.e. /news/article?id=1
>News Article - URL /news/article?id=1 -- Displays individual news articles, some may be blocked and accessible by premium users
>Contact Page - URL /contact -- Contains a form for customers to contact the company. It has named, email and message input fields and a send button
>Customers - URL /customers -- redirects to /customers/login
>Customer Login - URL /customers/login -- Contains a login form with username and password fields
>Customer Signup - URL /customer/signup -- Page contains a user-signup form that consists of a username, email, password, and password confirmation input fields
>Customer Reset Password - URL /customers/reset -- Password reset form with an email address input field
>Customer Dashboard - URL /customers -- contains a list of user's tickets submitted to the IT support company and a "Create Ticket" button
>Create Ticket - URL /customers/ticket/new -- Contains a form with a text box for entering the IT issue and a file upload option to create an IT support ticket.
>Customer Account - URL /customers/account -- Page allows users to edit their username, email and password
>Customer Logout - URL /customers/logout -- Logs customers out


>	Viewing the Page Source
>The page source is human-readable code returned to the browser from the web server each time a request is made. The code is made up of the main 3 websites languages (CSS, HTML, JS) and it tells the browser what content needs to be displayed, how to display it, and how to interact with it. Viewing the page source can help discover more information about the web application.
>	How to view the Page Source 
>1.  Right-clicking the page and clicking view page source
>2.  putting view-source in front of the URL for example, `view-source:https://www.google.com/`
>3.  In the browser menu, there's an option to view the page source. This option can sometimes be in submenus such as developer tools or more tools
>	Viewing the Page Source 
>Viewing the source is confusing as I do not know HTML to a wide extent, but I can pick out bits of information that are important. 
>Such as the `<!-- and -->` which specifies comments. 
>Links to different pages in HTML are written in anchor tags (`<a`), and the redirection link is stored in a href attribute.
>For example, the code
>![[Pasted image 20230925114424.png]]
>The links are wrapped by anchor tags and reference in href
>External files such as CSS, JavaScript and Images can be included using the HTML code. In this example, the files are all stored in the same directory, and viewing this gives a configuration error. What should be displayed is either a blank page or a 403 forbidden page with an error stating you don't have access to the directory. Instead, the directory listing feature has been enabled, which in fact, lists every file in the directory. Sometimes this isn't an issue, and all the files in the directory are safe to be viewed by the public, but in some instances, backup files, source code or other confidential information could be stored here. In this instance, we get a flag in the flag.txt file. 
>Many websites nowadays are made from a framework which is a collection of premade code that easily allows a developer that easily allows a developer to include common features that a website requires, such as blogs, user management, form processing, and much more, saving the developer hours or days of development. 
>Viewing the page source can give hints into whether a framework is in use and if so which framework and maybe what version. Knowing the framework and version can be a powerful find as there may be public vulnerabilities in the framework, and the website might not be using the most up-to-date version (zero days yesssss). Reading the update notice and using the information that you find to discover another flag.


>	Developer Tools - Inspector
>Every developer browser includes developer tools; This is a tool kit used to aid web developers in debugging web applications and gives you a peek under the hood of a website to see what is going on. As a pentester, we can leverage these tools to provide us with a much better understanding of the web application. We're specifically focusing on three features of the developer tool kit, inspector, Debugger and Network.
>	Opening Developer Tools
>The way to access developer tools is different for every browser. It can usually be accessed through the settings of the website.
>	Inspector
>The page source doesn't always represent what's shown on a webpage; This is because CSS, JS and user inspection can change the content and style of the page, which means we need a way to view what's been displayed in the browser window at the exact same time. Element inspector assists us with this by providing with a live representation of what is currently on the website. 
>As well as viewing this live view, we can also edit and interact with the page elements, which is helpful for web developers to debug issues. On the Acme IT Support website, click into the news section, where you'll see three news articles.
>The first two articles are readable, but the third has been blocked with a notice about how we need to be a premium user to access the content. 

>	Developer Tools - Debugger
>The panel in the developer tools is intended for debugging JS, but can be used by pentesters to dig deeper in JS code. In Firefox and Safari, this feature is called Debugger, but in Google Chrome, it's called sources. On the Acme IT support website, click on the contact page, each time the page is loaded, there's a rapid flash of red on the screen. We're going to use the Debugger to work out what this red flash is and if it contains anything interesting. Debugging a red dot wouldn't be used in the real world but helps us get used to this feature and get used to the Debugger. 

>	Developer Tools - Network
>The network tab on the developer tools can be used to keep track of every external request a webpage makes. If you click on the Network tab and then refresh the page, all the requested pages can be viewed.
>Try doing this on the contact page; the trash can icon can be used to delete the list if it gets a bit overpopulated. 