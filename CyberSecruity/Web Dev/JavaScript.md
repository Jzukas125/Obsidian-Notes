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

