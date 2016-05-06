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

But, by using `loop`, you can save your time and shorten your length of your code, which will look something like this : 

<?php
   for ($leap = 2004; $leap < 2050; $leap = $leap + 4) {
        echo "<p>$leap</p>";
      }
?>