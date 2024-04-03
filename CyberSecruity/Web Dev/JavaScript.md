Why Javascript?<br> Javascript is one of the 3 languages all web developers must learn:
1. HTML to define the content of web pages
2. CSS to specify the layout of web pages
3. JavaScript to program the behavior of web pages

# JavaScript Intro

One of JavaScript HTML methods is getElementById(). The example below "finds"  an HTML element (with id="demo"), and changes the element content (innerHTML) to "Hello :JavaScript":
```JavaScript
doucment.getElementById("demo").innerHTML = "Hello JavaScript";
```

This specific function would be used in tandem with HTML in button form such as 
```html
<!DOCTYPE html>
<html>
<body>

<h2> What Can JavaScript Do? </h2>

<p id ="demo">JavaScript can change HTML content </p>

<button type ="button" onclick='doucment.getElementById("demo").innerHTML = "Hello JavaScript!"'>Click me!</button>
```
JavaScript accepts both double and single quotes

JavaScript can change HTML attribute values such as 
```html
<!DOCTYPE html>
<html>
<body>

<h2>What Can JavaScript Do?</h2>

<p>JavaScript can change HTML attribute values.</p>

<p>In this case JavaScript changes the value of the src (source) attribute of an image.</p>

<button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">Turn on the light</button>

<img id="myImage" src="pic_bulboff.gif" style="width:100px">

<button
onclick="doucument.getElementById('myImage').src='pic_bulboff.gif'">Turn off the light </button>

</body>
</html>
```

JavaScript can change HTML styles (CSS)
`document.getElementById("demo").style.fontSize = "35px";`

JavaScript can Hide HTML Elements
`document.getElementById("demo").style.display="none"`;

JavaScript can show HTML elements
`document.getElementById("demo").style.display = "block";`

# JavaScript Where to

`<script>` tag
The script tag allows Javascript code to be inserted into HTML code.
```HTML
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```

JavaScript functions work like regular python or C++ fucntions

Any number of scripts can be placed in an HTML document. Scripts can be placed in the body, or in the head section of an HTML page, or in both.

JavaScript in Head
```html
<!DOCTYPE html>  
<html>  
<head>  
<script>  
function myFunction() {  
  document.getElementById("demo").innerHTML = "Paragraph changed.";  
}  
</script>  
</head>  
<body>

<h2>Demo JavaScript in Head</h2>  
  
<p id="demo">A Paragraph</p>  
<button type="button" onclick="myFunction()">Try it</button>

</body>  
</html>
```

JavaScript in body
```html
<!DOCTYPE html>
<html>
<body>

<h2>Demo JavaScript in Body</h2>

<p id="demo">A Paragraph.</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>

</body>
</html> 
```

Both of these have the same output with it changing the paragraph in the body, they're just written differently. 

Linking files
`<script src="/js/myScript.js"></script>`

# JavaScript Statements

```javascript
let x, y, z;    // Statement 1  
x = 5;          // Statement 2  
y = 6;          // Statement 3  
z = x + y;      // Statement 4
```

Javascript ignores whitespace

# JavaScript Syntax

JavaScript Syntax is as follows 
```JavaScript
//How to create variables:
var x;
let y;

//How to use variables:
x = 5;
y = 6;
let z = x + y;
```

Comments can be made using //

I am choosing to skip a majority of the teachings of w3 school in favor of learning what is applicable to my internship. I am utilizing a "fuck it we ball" methodology where I will write about things I will explain things in more detail if I do not understand them

# AJAX  Intro
Ajax is Asynchronous JavaScript And Xml
AJAX is a developer's dream, because it can:
- Read data from a web server after the page has loaded
- Updated a web page without reloading the page
- Send data to a web server in the background
- AJAX is a technique for asscessing web servers from a web page
- AJAX stands for Asynchronous JavaScript and XML

HTML Page
```html
<!DOCTYPE HTML>
<html>
<body>

<div id="demo">
	<h2> Let AJAX change this text </h2>
	<button type="button" onclick="loacDoc()">Change Content </button>
</div>

</body>
</html>
```

The HTML page contains a `<div>` section and a `<button>`
The `<div>` section is used to display information from a server.
The `<button>` calls a function (if it is clicked).
The function requests data from a web server and displays it:

Function loadDoc()
```JavaScript
function loadDoc(){
	const xhttp = new XMLHttpRequest();
	xhttp.onload = function() {
	document.getElementById("demo").innerHTML = this.responseText;
	}
	xhttp.open("GET","ajak_info.txt",true);
	xhttp.send();
}
```

![[Pasted image 20240403113301.png]]
1. An event occurs in a web page
2. An XMLHttpRequest object is created by JavaScript
3. The XMLHttpRequest object sends a request to a web server
4. The server processes the request
5. The server sends a response back to the web page
6. The response is read by JavaScript
7. Proper action is performed by JavaScript

# AJAX - The XMLHttpRequestObject

The Keystone of AJAX is the the XMLHttpRequest object.
1. Create an XMLHttpRequest object
2. Define a callback function
3. Open the XML