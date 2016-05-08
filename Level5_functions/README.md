#Level5_functions
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