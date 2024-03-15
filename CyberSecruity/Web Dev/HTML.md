# Intro
HMTL stands for Hyper Text Markup Language, standard markup language for creating web pages, HTML describes the structure of a Web page, consists of a series of elements, elements tell the browser how to display content, elements label pieces of content such as "this is a heading", "this is a paragraph", "This is a link", etc.

My first HTML Document
```html
<!DOCTYPE html>
<html>
<head>
<title> Page Title </title>
</head>
<body>

<h1> My First Heading </h1>
<p> my first paragraph. </p>

</body>
</html>
```

<html>
<head>
<title> Page Title </title>
</head>
<body>

<h1> My First Heading </h1>
<p> my first paragraph. </p>

</body>
</html>

What is an HTML element? 
an HTML element is defined by a start tag, some content, and an end tag:
```
<tagname> Content goes here ... </tagename>
```

The HTML element is everything from the start tag to the end tag:
```html
<h1> My first heading </h1>
<p> My first paragraph </p>
```

# Skipping basic HTML as I already know it

# HTML Forms

the form Element is used to create an HTML form for user input:
```HTML
<form>
.
form elements
.
</forms>
```

The form element is a container for different types of input elements, such as: text fields, checkboxes, radio buttons, submit buttons, etc.

# The Input Element 
The HTML input element is the most used form element. An input element can be displayed in many ways, depending on the type attribute.

# Text Fields
The `<input type="text>` defines a single-line input field for text input.
Example:
```html
<form>
	<label for="fname">First name: </label><br>
	<input type="text" id="fname" name="fname"><br>
	<label for="lname">Last name:</label><br>
	<input type="text" id="lname" name="lname">
```

# The Label Element 
As you can tell the label element is used in the above example code. The label tag defines a label for many form elements. 