# Level 1 : Introduction to PHP

## PHP syntax 
### 1. Echo 
The echo function outputs strings. If you type

```php

<?php
  echo "Hello!";
?>

```
PHP will output **Hello!**.

### 2. Strings 

A string is a word or phrase between quotes, like so: **"Hello, world!"**

You can type a string all at once, like this:

```php

<?php
  echo "Hello, world!";
?>

```

Or use the **concatenation operator**, which glues several strings together:

```php

<?php
  echo "Hello," . " " . "world" . "!";
?>

```

### 3. Arithmetic

In addition to outputting strings, PHP can also do math.

```php

<?php
  echo 5 * 7;
?>

```
Here we use **echo** to multiply 5 and 7, and we end our line of code with a semicolon. PHP will output **35**.

### 4. Variables 

So far we've been outputting strings and doing math.

To do more complex coding, we need a way to "save" these values. We can do this using variables. A **variable** can store a string or a number, and gives it a specific case-senstive name.

**Examples:**
```php

<?php
	$myName = "Beyonce";
	$myAge = 32;
?>

```

All variable names in PHP start with a dollar sign `( $ )`.

### 5. Comments 

Just like we sometimes put comments in our CSS `(using /* this syntax */)` or in our HTML `(using <!-- this syntax -->)`, we can also put comments in our PHP code! We do that using two forward slashes `(//)`, like so:

```PHP

<?php
	echo "I get printed!";
	// I don't! I'm a comment.
?>

```

### 6. Echo Variable 

```PHP

<?php
	$myName = "bla";
	$myAge = 7;
	echo $myName;
	echo $myAge;
?>

```
Output : `Bla7`