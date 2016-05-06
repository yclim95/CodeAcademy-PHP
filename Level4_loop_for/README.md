# Level4_loop_for
## What is a loop?

Normally, if you want to display out a lot of output. You will write something like this :

```php
<?php
 echo 2004;
 echo 2008;
 echo 2012;
 // And so on
?>
```

### 1. For Loop
But, by using `loop`, you can save your time and shorten your length of your code, which will look something like this : 

```php
<?php
  for ($leap = 2004; $leap < 2050; $leap = $leap + 4) {
        echo "<p>$leap</p>";
      }
?>
```

### 2. ForEach = Loops + Arrays 

The `foreach` loop is used to iterate over each element of an object—which makes it perfect for use with arrays!

You can think of `foreach` as jumping from element to element in the array and running the code between `{}`s for each of those elements.

E.G: 

```php
<?php
 $langs = array("JavaScript",
          "HTML/CSS", "PHP",
          "Python", "Ruby");
        
          foreach ($langs as $lang) {
              echo "<li>$lang</li>";
          }
        
          unset($lang);
?>
```

```php
** Output **
1. JavaScript 
2. HTML/CSS
3. PHP 
4. Python 
5. Ruby 
```