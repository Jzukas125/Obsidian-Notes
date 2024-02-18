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
