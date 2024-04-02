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

