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
$x = 5
$y = "John"
```
In this example the v