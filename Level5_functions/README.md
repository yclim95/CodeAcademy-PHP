#Level5_functions part 1
## What is functions ?
Functions are `reusable` pieces of code that you can use throughout an application, saving you lots of copying and pasting.

PHP has lots of built-in functions, and we'll learn some of them in these exercises. The first set of functions we'll learn about are string manipulation functions.

## String manipulation functions 
### 1. Strlen()
one of the most common String functions in PHP. You pass it a string, or variable containing a string, and it returns the number of characters in that string. An example might be:

```php
<?php
  // get the length of a string and
  // print it to the screen
  $length = strlen("david");
  print $length;
?>
```

### 2. Substr()
This function allows you to return a substring (piece of) of your string.

You pass this function the string you want to get a substring of, the character in your string to start at, and how many characters you want after your starting point. An example might be:

```php
<?php
  $myname = "David";

// you can manipulate strings easily
// with built-in funtions too
$partial = substr($myname, 0, 3);
print $partial;
// prints "dav"
?>
```

**NOTE:** *the second parameter (the starting character) is based on a zero-indexed array (i.e. the first character in your string is number 0, not number 1)*.


### 3. Strtoupper()/ Strtolower()
make your entire string *UPPERCASE* or *lowercase*.

```php
<?php
$uppercase = strtoupper($myname);
print $uppercase;
// prints "DAVID"

$lowercase = strtolower($uppercase);
print $lowercase;
// prints "david"
?>
```

### 4. Strpos()
Find the position of the first occurence of a substring in a string.

```php
<?php
strpos("emily", "e");   // 0
strpos("emily", "i");   // 2
strpos("emily", "ily"); // 2
strpos("emily", "zxc"); // false
?>
```
The parameters passed to `strpos()` are the `haystack` and the `needle`. The function tries to find the needle in the haystack.

It returns either the index of the first character, or `false` if the needle cannot be found.

```php
<?php
if (strpos("david","h") === false) {
  print "Sorry, no 'h' in 'david'";
}
// prints the "Sorry" message
?>
```

## Maths functions 
### 1. Round()
This function rounds floating point numbers (numbers with decimal points in them) up or down.

You can also use round() to round your number to an integer, or to round off complex floating point numbers to a specific number of decimal places. This is accomplished by passing a second, optional parameter to round(), telling it how many decimal places you want the number rounded to.

Here's an example : 

```php
<?php
// Round pi down from 3.1416...
$round = round(M_PI);
print $round;  // prints 3

// This time, round pi to 4 places
$round_decimal = round(M_PI, 4);
print $round_decimal; // prints 3.1416
?>
```
**NOTE**: `M_PI` is a PHP constant that is equal to pi.


### 2. Rand()

This function returns a random number between two numbers. Optionally, you can provide your `min` & `max` numbers as parameters, like this:

```php
<?php
// prints a number between 0 and 32767
print rand();

// prints a number between 1 and 10
print rand(1,10);
?>
```

## Array functions 
### 1. Array_push()
Is arguably the most common and useful function for manipulating arrays.

`array_push()` takes two arguments: an array, and an element to add to the end of that array.Here's an example:

```php
<?php
$fav_bands = array();
array_push($fav_bands, "Maroon 5");
array_push($fav_bands, "Bruno Mars");
array_push($fav_bands, "Nickelback");
array_push($fav_bands, "Katy Perry");
array_push($fav_bands, "Macklemore");
?>
```

###2. Count()
Will return the `number` of elements in that array. Like this:

```php
<?php
print count($fav_bands); // prints 5
?>
```

###3. Sort()
```php
<?php
$array = array(5, 3, 7, 1);
sort($array);
print join(", ", $array);
// prints "1, 3, 5, 7"
?>
```

PHP also has the `opposite` function: `rsort()`
```php
<?php
$array = array(5, 3, 7 ,1);
rsort($array);
print join(":", $array);
// prints "7:5:3:1"
?>
```

#Level5_functions part 2
## Function syntax 

The typical structure of a function is as follows:

```php
<?php
function name(parameters) {
  statement;
}
?>
```

1. The `keyword` function indicates that the code following it will be a user-defined function.

2. `name` indicates the name of a function, which is case insensitive. The name of a function can contain numbers, letters, underscores or dashes.

3. The **arguments**, or **parameters**, will be the optional input a function uses to perform calculations.

4. And of course, the **statements** themselves will be the code the function executes when it is called.

### 1. RETURN keywords 

Instead of printing something to the screen, what if you want to make it the value that the function outputs so it can be used elsewhere in your program? In PHP, the return keyword does just that. It returns to us a value that we can work with. 
The difference between this and `echo` or `print` is that it doesn't actually display the value.

Put in a simple way, just like a calculator u solve the mathematical problem $ it takes several steps to solve it. The value from is each step is computed. BUT, we dont get to see the results, until we get to see the final answer. 

```php
<?php
 function returnName(){
            return "lala";
        }
        
        print returnName(); //Call function 
?>
```

### 1. Parameters & Arguments 

Functions is pretty useful as you have seen the syntax of functions introduced above. BUT, it won't be that useful or full utilized UNLESS you have use the **parameters** & **arguments**. 

These are the variables or inputs that a function uses to perform calculations.

**Sample 1:** 

```php
<?php
function squareValue($number) {
  echo $number * $number;
} 

$n = 6;
squareValue($n); // echos 36
?>
```

The function `squareValue`, above, takes one parameter, which it multiplies by itself and then echos the result. The names of the parameters themselves are used internally within the function, so they should be named something helpful.

**Sample 2:** 

```php
<?php
function greetings($name){
  echo "Greetings, " . $name . "!";
}

greetings("George");
?>
```