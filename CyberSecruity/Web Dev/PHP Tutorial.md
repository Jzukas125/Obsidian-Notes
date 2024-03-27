I am taking notes to learn PHP while using the w3schools tutorial found at https://www.w3schools.com/php/default.asp

User https://www.programiz.com/php/online-compiler/ to compile PHP
# PHP syntax
basic PHP syntax is 
```php
<?php
echo "Hello World!";
?>
```

# PHP Intro

PHP is an acronym for "PHP: Hypertext Preprocessor"
PHP is widely-used, open source scripting language
PHP scripts are executed on the serve and it is free to download and use

Powerful enough to be on the biggest blogging system on the internet which is WordPress, deep enough to run large social networks, and is easy enough to be a beginner's first server side language.

PHP files can contain text, HTML, CSS, JavaScript, and PHP code. PHP code is executed on the server, and the result is returned to the browser as plain HTML.

PHP can generate dynamic content, it can create, open, read, write, delete, and close files on the serer. It can collect form data, send and receive cookies, add, delete, and modify data in your database. PHP can be used to control user-access and can encrypt data.

PHP runs on various platforms, is compatible with more servers, supports a wide range of databases, is free, and is easy to learn while running efficiently on the server side 

# Basic syntax

```php
<?php
//PHP code goes here
```
A PHP script starts with `<?php and ends with ?>` 
Default file extension is .php and a php file usually contains HTML tags, and some PHP scripting code

Here is an example of a simple .php file with HTML and PHP code
```php
<!DOCTYPE html>
<html>
<body>

<h1>My first PHP page</h1>

<?php
echo "Hello World!";
?>

</body>
</html>
```

PHP is NOT case sensitive so 
ECHO
echo 
EchO
eCHO
are all the same but all variable names are case sensitive

For example

```php
<!DOCTYPE html>
<html>
<body>

<?php$color = "red";
ecHo "My car is " . $color . "<br>";
ECHO "My house is " . $COLOR . "<br>";
echo "My boat is " . $coLOR . "<br>";
?>

</body>
</html>
```

would output 
```
My car is red
My house is 
My boat is 
```

Reminder: every command in PHP needs a ; behind it
# PHP comments

PHP comments range from
```php
// php comment
#php comment
/* multi 
line 
comment */

```

# PHP Variables
Variables are containers for storing information

In PHP a variable starts with the $ sign, followed by the name of the variable such as 
```php
$x = 5;
$y = "John";
```
In this example the variable $x will hold the value 5, and the variable $y will hold the "john" value.

Outputting variables
the PHP echo statement is often used to output data to the screen and the following examples will show how to output text and a variable:
```php
$txt = "JacobizCul.com";
echo"I love $txt!";
```

 This is the same as typing 
 
 ```php
$txt = "JacobizCul.com";
echo "I love " . $txt . "!";
```

This example will output the sum of two variables
```php
$x = 5;
$y = 4;
echo $x + $y;
```

PHP does not require to tell what data type a variable is although they can be declared and we will learn about strict and non-strict requirements later on in the PHP functions chapter.

PHP has no command for declaring variable types, and the data type depends on the value of the variable 
```php
$x = 5;
$y = "John";
echo $x;
echo $y;
```

The var_dump() function can return the data type of a variable such as 
```php
$x = 5;
var_dump($x);
```

var_dump can also return what type of data something is just from its entry such as 
```php
var_dump(5);
var_dump("John");
var_dump(3.14);
var_dump(true);
var_dump([2, 3, 56]);
var_dump(NULL);
```
with it outputting 
```
int(5)
string(4) "John"
float(3.14)
bool(true)
array(3) {
  [0]=>
  int(2)
  [1]=>
  int(3)
  [2]=>
  int(56)
}
NULL
```

You can assign multiple variables in one line using 
```php
$x = $y = $z = "Fruit";

echo $x;
echo $y;
echo $z;
```

With all of them outputting fruit 

# Variables Scope

The scope of a variable is the part of the script where the variable can be reference/used
PHP has three different variable scopes: 
	Local 
	Global 
	Static

Global and Local Scope
A variable declared outside a function has a GLOBAL SCOPE can can only be accessed outside a function

```php
$x = 5; // global scope

function myTest() {
  // using x inside this function will generate an error
  echo "<p>Variable x inside function is: $x</p>";
}
myTest();

echo "<p>Variable x outside function is: $x</p>";
```

A variable declared within a function has a local scope and can only be accessed within that function

```php
function myTest() {
  $x = 5; // local scope
  echo "<p>Variable x inside function is: $x</p>";
}
myTest();

// using x outside the function will generate an error
echo "<p>Variable x outside function is: $x</p>";
```

The global keyword is used to access a global variable from within a function. To do so the global keyword should be used before a variable.

```php
$x = 5;
$y = 10;

function myTest() {
  global $x, $y;
  $y = $x + $y;
}

myTest();
echo $y; // outputs 15
```

PHP also stores all global variables in an array called $GLOBALS[index]. The index holds the name of the variable. This array is also accessible from within functions and can be used to update global variables directly.

```php
$x = 5;
$y = 10;

function myTest(){
	$GLOBALS['y'] = $GLOBALS['x'] + $GLOBALS['y'];
}

myTest();
echo $y; //outputs 15
```

PHP static keyword 

Normally when a function is completed/executed, all of its variables are deleted. However, sometimes we want a local variable NOT to be deleted. We need it for a further job.
To do this, use the static keyword when you first declare the variable

```php
function myTest() {
	static $x = 0;
	echo $x;
	$x++;
}

myTest();
myTest();
myTest();
```

# PHP echo and print statements

echo and print are the two ways to get output for PHP. This chapter contains a little more info about it.

echo and print are more or less the same. They are both used to output data to the screen.

The differences are small: echo has no return value while print has a return value of 1 so it can be used in expressions. eco can take multiple parameters while print can take one argument. echo is marginally faster than print.

The echo statement can be used with or without parentheses: echo or echo()

```php
echo "<h2>PHP is Fun!</h2>";
echo "Hello world!<br>";
echo "I'm about to learn PHP!<br>";
echo "This ", "string ", "was ", "made ", "with multiple parameters.";
```

echo can also output text and variables with the echo statement: 

```php
$txt1 = "Learn PHP";
$txt2 = "W3Schools.com";
$x = 5;
$y = 4;

echo "<h2>" . $txt1 . "</h2>";
echo "Study PHP at " . $txt2 . "<br>";
echo $x + $y;
```

print can do all the same with the exact same syntax but it is just slower.

# PHP Data Types

PHP supports the following data types:
	String
	Integer
	Float
	Boolean
	Array
	Object
	NULL
	Resource
	
var_dump can be used to get the data type of a function.

A string is a sequence of characters

A PHP integer is a non-decimal number between 2,147,483,648 and 2,147,483,647.

Rules for an integers:
- An integer must have at least one digit
- an integer must not have a decimal point
- an integer can be either positive or negative
- Integers can be specified in: decimal (base10), hexadecimal (base16), octal (base 8), or binary (base 2) notation

In this example $x is an integer and the PHP var_dump() function returns the data type and value:
```php
$x = 5985;
var_dump($x);
```

PHP float is a number with a decimal point or a number in exponential form.
Example:
```php
$x = 10.365;
var_dump($x);
```

A Boolean represents two possible states: TRUE or FALSE

```php
$x = true;
var_dump($x);
```
Booleans are using in conditional testing

PHP arrays store multiple values in a single variable
Example:
```php
$cars = array("Volvo", "BMW", "Toyota");
var_dump($cars);
```

PHP is an OOP with a class being a template for objects, and an object being an instance of a class. 

When the individual objects are created, they inherit all the properties and behaviors from the class, but each object will have different values for the properties

Let's assume we have a class named Car that can have properties like model, color, etc. We can define variables like $model, $color, and so on, to hold the values of these properties. 

When the individual objects are created, they inherit all the properties and behaviors from the class, but each object will have different values for the properties. 

If you create a `__construct()` function, PHP will automatically call this function when you create an object from a class.

```php
class Car {
public $color;
public $model;
public function __construct($color, $model){
   $this->color = $color;
   $this->model = $model;
   }
   public function message(){
   return "My car is a " . $this->color ." ". $this->model . "!";
   }
}

$myCar = new Car("red","Volvo");
var_dump($myCar);
```

The PHP Null value is a special data type which can have only one value: NULL.
A variable of data type NULL is a variable that has no value assigned to it.
Variables can also be emptied by setting the value to NULL:

```php
$x = "Hello world!";
$x = null;
var_dump($x);
```

Data type is changed by which ever it was assigned to last, to avoid this you can use casting.
Casting allows you to change data types on variables
```php
$x = 5;
$x = (string) $x;
var_dump($x);
```

The PHP resource type is not an actual data type. It is the storing of a reference to functions and resources external to PHP. 
A common example of using the resource data type is a database call. Will not be talked about here, as it is an advanced topic.

# PHP strings 
A string is a sequence of characters, like "Hello World"

Double quotes preform an action on special characters like calling a variable while single quotes do the literal output

```php
$x = "John";
echo "Hello $x";
echo 'Hello $x';
```

strlen() returns the length of a string

```php
echo strlen("Hello world");
echo strlen("This string is characters long");
```

The PHP str_word_count() function counts the number of words in a string

```php
echo str_word_count("Hello world!");
```

The PHP strpos() function searches for a specific text within a string
If a match is found, the function returns the character position of the first match. If no match is found, it will return FALSE

Example:
```php
echo strpos("Hello world!", "world");
```

# PHP modify strings

strtoupper() function returns everything in the uppercase
strtolower() function returns the sting in lower case

```php
$x = "Hello World!";
echo strtoupper($x);
echo strtolower($x);
```

The PHP function str_replace() replaces some characters with other characters in a string

```php
$x = "Hello World!";
echo str_replace("World","Wolly", $x);
```

The PHP function strrev() function reverses a string

```php
$x = "Hello World!";
echo strrev($x);
```

The PHP function trim() removes any whitespace from the beginning or the end

```php
$x = " Hello World! ";
echo trim($x);
```

The PHP function explode() splits a string into an array with the first parameter of the explode() function representing the "separator". The "separator" specifies where to split the string.

```php
$x = "Hello World!"
$y = explode(" ", $x);

//have to use print_r to see results
print_r($y);
```

To concatenate strings you need to use the . operator 

```php
$x = "Hello";
$y = "World";
$z = $x . $y;
echo $z;
```

and adding a space looks like this

```php
$x = "Hello";
$y = "World";
$z = $x . " " . $y;
echo $z;
```

An easier way of doing this would be to use the power of double quotes. By surrounding the two variables in double quotes with a white space between them, the white space will also be present in the result:

```php
$x = "Hello";
$y = "World";
$z = "$x $y";
echo $z;
```

Slicing can return a range of characters by using the substr() function and you can specify the start index and the number of characters you want to return.

```php
$x = "Hello World!";
echo substr($x, 6, 5);
```
This example starts the index at 6 and ends the slice 5 positions later thus cutting out the word "Hello".

To insert characters that are illegal in a string use an escape character such as 

```php
$x = "We are the so-called \"Vikings\" from the north.";
```
This shows the word Vikings in quotes without destroying the php string

Check if a number in PHP is an integer using var_dump(is_int)($x)) such as:

```php
$x = 5985;
var_dump(is_int($x));

$x = 59.85;
var_dump(is_int($x));
```

Casting statements from one to another requires it to be declares as so:

```php
$a = 5;       // Integer
$b = 5.34;    // Float
$c = "25 kilometers"; // String
$d = "kilometers 25"; // String
$e = "hello"; // String
$f = true;    // Boolean
$g = NULL;    // NULL

$a = (int) $a;
$b = (int) $b;
$c = (int) $c;
$d = (int) $d;
$e = (int) $e;
$f = (int) $f;
$g = (int) $g;
```

This can be done with any data type and only requires to change the int to which ever data type you would like

PHP math includes pi, min, max, abs, sqrt, round, and rand.

A PHP constant is an identifier for a simple value. The value cannot be changed during the script.
A valid constant name starts with a letter or underscore

To create a constant use the define() function

```php
define(name, value, case-insensitive);
```
Parameters define as:
	name: specifies the name of the constant
	value:  specifies the value of the constant
	case-insensitive: Specifies whether the constant name should be case-insensitive. Default is false 

Example of creating a constant with a case-sensitive name:
```php
define("GREETING", "Welcome to W3Schools.com~");
echo GREETING;
```

Create a constant with a case-insensitive name:
```php
define("GREETING", "Welcome to W3Schools.com!", true);
echo greeting;
```

You can also create a constant using the const keyword

```php
const MYCAR = "Volvo";
echo MYCAR
```

From PHP, you can create an array constant by using the define() function

```php
define("cars", [
  "Alfa Romeo",
  "BMW",
  "Toyota"
]);
echo cars[0];
```

Constants are automatically global and can be used across the entire script

```php
define("GREETINGS", "Welcome to W3Schools.com!");

function myTest() {
   echo GREETING;
}

myTest();
```

# PHP Magic Constants

```
## Magic Constants

Here are the magic constants, with descriptions and examples:

|Constant|Description||
|---|---|---|
|__CLASS__|If used inside a class, the class name is returned.|[Try it »](https://www.w3schools.com/php/phptryit.asp?filename=tryphp_const_class)|
|__DIR__|The directory of the file.|[Try it »](https://www.w3schools.com/php/phpshowit.php?filename=tryphp_const_dir)|
|__FILE__|The file name including the full path.|[Try it »](https://www.w3schools.com/php/phpshowit.php?filename=tryphp_const_file)|
|__FUNCTION__|If inside a function, the function name is returned.|[Try it »](https://www.w3schools.com/php/phptryit.asp?filename=tryphp_const_function)|
|__LINE__|The current line number.|[Try it »](https://www.w3schools.com/php/phptryit.asp?filename=tryphp_const_line)|
|__METHOD__|If used inside a function that belongs to a class, both class and function name is returned.|[Try it »](https://www.w3schools.com/php/phptryit.asp?filename=tryphp_const_method)|
|__NAMESPACE__|If used inside a namespace, the name of the namespace is returned.|[Try it »](https://www.w3schools.com/php/phptryit.asp?filename=tryphp_const_namespace)|
|__TRAIT__|If used inside a trait, the trait name is returned.|[Try it »](https://www.w3schools.com/php/phptryit.asp?filename=tryphp_const_trait)|
|ClassName::class|Returns the name of the specified class and the name of the namespace, if any.|
```

PHP comparison operators
PHP comparison operators use three symbols instead of two
Operator	Name	Example	Result
Equal	$x == $y	Returns true if $x is equal to $y	
Identical	$x === $y	Returns true if $x is equal to $y, and they are of the same type
Everything else works similar to C++ or python

PHP conditional statements such as an if statement is similar to C++ and looks like

```php
$t = 14;

if ($t == 14) {
  echo "Have a good day!";
}
```

Logical operators also operate the same as they do in C++, with the operators being:
Operator	Name	Description	
and And	 True if both conditions are true	
&&	And	True if both conditions are true	
or	Or	True if either condition is true	
||	Or	True if either condition is true	
xor	Xor	True if either condition is true, but not both	
!	Not	True if condition is not true

The if ...else statement also functions similarly to C++ but the if ... elseif haing a difference with it looking like:

```php
$t = date("H");

if ($t < "10") {
  echo "Have a good morning!";
} elseif ($t < "20") {
  echo "Have a good day!";
} else {
  echo "Have a good night!";
}
```

Short hand if else statments also function similar to C++ with an if else statement being:

```php
$a = 13;

$b = $a < 10 ? "Hello" : "Good Bye";

echo $b;
```

PHP switch statement also functions similar to C++ and looks like:
```php
$favcolor = "red";

switch ($favcolor) {
  case "red":
    echo "Your favorite color is red!";
    break;
  case "blue":
    "Your favorite color is blue!";
    break;
  case "green":
    echo "Your favorite color is green!";
    break;
  default:
    echo "Your favorite color is neither red, blue, nor green!";
}
```

The default keyword specifies the code to run if there is no case match. If no cases get a match the default block is executed like so:

```php
$d = 4;

switch ($d) {
  case 6:
    echo "Today is Saturday";
    break;
  case 0:
    echo "Today is Sunday";
    break;
  default:
    echo "Looking forward to the Weekend";
}
```

Putting the default block at any other place than the end is not suggested such as in the beginning or in the middle

PHP while loops are very similar to C++ and look as such:

```php
$i = 1;
while ($i < 6) {
  echo $i;
  $i++;
}
```
A break statement can stop the loop even if the condition is still true


# Including PHP in HTML
Not only can php be used in tandem with HTML it can also be used ***in*** HTML. Meaning you can put php lines in HTML statements such as:
```php
<!DOCTYPE html> 
<html> 
  
<head> 
    <style> 
        h1 { 
            color: green; 
        } 
    </style> 
</head> 
  
<body> 
    <center> 
        <h1>Welcome To GFG</h1> 
  
        <h2> 
            <?php  
            echo "This is PHP code inside html"
            ?> 
        </h2> 
    </center> 
</body> 
  
</html> 
```

# PHP Form Handling
The PHP super global $_GET and $_POST are used to collect form-data.

A simple HTML form example would look like 
```html
<html> 
<body>

<form action="welcome.php" method="POST">
Name: <input type="test" name="name"><br>
E-mail: <input type="text" name="email"><br>
</form>

</body>
</html>
```
When the user fills out the form above and clicks the submit button, the form data is sent for processing for a PHP file named "welcome.php". The form data is sent with the HTTP POST method. 

To display the submitted data you could simply echo all the variables.

The "welcome.php" looks like this
```PHP
<html>
<body>

Welcome <?php echo $_POST["name"]; ?> <br>
Your email address is: <?php echo $_POST["email"]; ?>

</body>
</html>
```


The output would look like:
```
Welcome John
Your email address is john.doe@example.com
```

The same result could also be achieved using the HTTP GET method:
```php
<html>
<body>

<form action="welcome_get.php" method="GET'>
Name: <input type="text" name="name"><br>
E-mail: <input type="text" name="email"><br>
<input type="submit">
</form>

</body>
</html>
```

and "welcome_get.php" looks like this:
```php
<html>
<body>

Welcome <?php echo $_GET["name"]; ?><br>
Your email address is: <?php echo $_GET["email"]; ?>

</body>
</html>
```

The code above is quite simple although it does not include any validation.
You need to validate form data to protect your script from malicious code.

<h3> GET vs. POST </h3>
Both GET and POST request create an array. This array holds key/value pairs, where keys are the names of the form controls and values are the input data from the user. 

Both Get and POST are treated as $_GET and $_POST. These are superglobals, which means that they are always accessible, regardless of scope - and you can access them from any function, class or file without to do anything special.

***`$_GET` is array of variables passed to the current script via the URL parameters.
`$_POST` is an array of variables passed to the current script via the HTTP POST method***

<h3> When to use GET? </h3>
Information from a form with the GET method is visible to everyone. GET also has limits on the amounts of information to send. The limitation is about 2000 characters. However, because the variables are displayed in the URL, it is possible to bookmark the page. This can be useful in some cases.

GET may be used for sending non-sensitive data.

<h3> When to use POST? </h3>
Information from a form with the POST method is invisible to others and has no limits on the amount of information to send.

Moreover POST supports advanced functionality such as support for multi-part binary input while uploading files to server. However, because the variables are not displayed in the URL, it is not possible to bookmark the page.

# PHP Form Validation
The validation rules are as follows:
Field - Validation Rules
Name - Required. + Must only contain letters and whitespace
E-mail - Required + Must contain a valid email address (with @ and .)
Website - Optional. If present, it must contain a valid URL
Comment - Optional. Multi-line input field (textarea)
Gender - Required. Must select one

<h3> Text Fields </h3>
HTML code looks like this:
```php
Name: <input type="text" name="name">
E-mail: <input type="text" name="email">
Website: <input type="text" name="website">
Comment: <textarea name="comment" rows="5" cols="40"></textarea>
```

<h3> The Form element </h3>
The HMTL code of the form looks like:
```php
<form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
```

When the form is submitted, the form data is sent with method="post".

