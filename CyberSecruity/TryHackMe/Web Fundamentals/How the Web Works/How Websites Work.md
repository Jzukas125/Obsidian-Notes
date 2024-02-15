>	How websites work
>In this room we will be learning how websites and created and learn some basic security issues. When visiting a website, the browser being used makes a request to the server asking for information about the page being visited. It will respond with data that your browser uses to show you the page.
>The two major components that make up a website are the front end (how a browser is rendered) and back end (a server that processes your request and returns a response). 
>Processes are more complex in making a request, but this is all we need to understand for now


>	HTML
>Websites are made using mostly:
>HTML - Defines the structure 
>CSS - makes website look pretty by adding styling options
>JavaScript - Implements complex features on pages using interactivity 
>Hyper Text Markup Language is the language websites are written (sometimes markdown too, but we're not talking about that). Elements aka tags tell the browser how to display content. This example displays a simple HTML document.
>![[Pasted image 20230921152901.png]]
>	The HTML structure is as follows:
><!DOCTYPE HTML>  defines the page as an HTML5 document which helps with standardization across different browsers and tells the browser to use HTML5 to interpret the page. 
> `<html>` element is the root element of the HTML page - all other elements come after this 
> `<head>` tag contains the information about the page
> `<body>` element defines the HTML document's body; **Only what is in the body is shown on the page
> `<h1>` element defines a large heading (the number determines the size of the header with the bigger number being smaller)
> `<p>` tag defines a paragraph
> This just cover the most basic tags and there are still many more to discover.
> tags can contain attributes such as the class attribute, which can be used to style an element `<p class = "bold-text"` and the src attribute is used on images to specify the location, such as `<img src = "img/cat.jpg"`. An element can have multiple attributes, each with its own unique purpose, e.g. `<p attribute1 = "value1" attribute2="value2"`
> Elements can also have an ID attribute which is unique to the element. Unlike the class attribute, an element must have different ID's to identify them uniquely. Element IDs are used for styling and to identify it by JavaScript


>	JavaScript 
>JS allows HTML pages to be interactive, by controlling the functionality of web pages without JavaScript, a page would not have interactivity and would always be static. JS can dynamically update the page in real-time, giving functionality to change the style of a button when a particular even on the page occurs or to display moving animations. 
>JavaScript is added in the page's source code and can be loaded within `<script>` tags or can be included remotely with the src attribute: `<script src="/location/of/javascript_file.js"></script>`
>The following JavaScript code finds an HTML element on the page with the ID of "demo" and changes the element's contents to "Hack the Planet" :document.getElementbyId("demo").innerHTML = "Hack the Planet";
>HTML elements also have onclick events that execute JavaScript when the event occurs. The following code changes the text of an element with the demo ID to Button Clicked: `<button 1 onclick='document.getElementById("demo").innerHTML = "Button Clicked";'> Click Me! </button>` 


>	Sensitive Data Exposure
>Sensitive Data Exposure occurs when a website doesn't properly protect sensitive clear-text information to the end-text. Due to HTML tags the entire source code can be viewed by inspecting and a website developer may have forgotten to remove login credentials, hidden links to private parts of the website or other sensitive data shown in HTML or JavaScript. Sensitive info can be leveraged to further an attacker's access within different parts of a web application. Whenever viewing a web app for security issues, one of the first things is to review the page's source code to see if any login credentials are exposed.


>	HTML Injection
>HTML injection is a vulnerability that occurs when unfiltered user input is displayed on the page. If a website fails to sanitize user input, and that input is used on the page, an attacker can inject HTML code into a vulnerability website. Input sanitization is important in keeping a website secure, as information a user inputs into a website is often used in other frontend and backend functionality. Soon we'll learn database injection, where we can manipulate database queries. When a user has control of how their input is displayed, they can submit HTML code, and the browser will use it on the page, allowing the user to control the page's appearance and functionality. Whatever a user inputs into a field that is passed to a JavaScript function and output to the page, which means if the user adds their own HTML or JavaScript in the field, it's used in the function and is added to the page, meaning you can add your own HTML, and it will output pure HTML. A general rule is to never trust user input. To prevent malicious input, the website developer should sanitize everything the user enters before using it in the JavaScript function; in this case, the developer could remove any HTML tags.
>`<a href = website_link> </a> ` Is usually used for basic injection.