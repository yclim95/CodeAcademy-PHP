# Level 2 Control Structure

## PHP Control Flow 

### 1. Comparison 

List of comparison operators:

* `>` Greater than
* `<` Less than
* `<=` Less than or equal to
* `>=` Greater than or equal to
* `==` Equal to
* `!=` Not equal to

### 2. If Statements  

Say we want to write a program that asks whether your name is longer than 7 letters. If the answer is yes, we can respond with "You have a long name!" We can do this with an if statement:

```php

<?php
   $age = 17;

  if( $age > 16 ) {
    echo "You can drive!";
  }
?>
```
An `if` statement is made up of the if keyword, a condition like we've seen before, and a pair of curly braces `{ }`. If the answer to the condition is yes, the code inside the curly braces will run.

### 3. If Else Statements  

Great! We used an if statement to do something if the answer to the condition was yes, or true as we say in PHP.

In addition to doing something when the condition is true, we can do something else if the condition is `false`. We can do this using an `if / else` statement:

```php

<?php
  $name = "Edgar";

  if ($name == "Simon") {
    print "I know you!";
  }
  else {
    print "Who are you?";
  }
?>
```

Just like before, if the condition is true, then only the code inside the first pair of curly braces will run. Otherwise, the condition is false, so only the code inside the second pair of curly braces after the else keyword will run.

In the example above the condition $name == "Simon" evaluates to false since $name is Edgar. Since the condition is false, only the code inside the curly braces after the else keyword runs, and prints out `Who are you?`

### 4. Switch Statements 

A switch statement comes in handy when you have a series of `if/elseif/else` statements with multiple expressions that depend on the same value. The switch statement also provides a bit of efficiency and readability. Switches work like if statements, if a condition is true, it executes a block of code.

```php
<?php
    switch (2) {
        case 0:
            echo 'The value is 0';
            break;
        case 1:
            echo 'The value is 1';
            break;
        case 2:
            echo 'The value is 2';
            break;
        default:
            echo "The value isn't 0, 1 or 2";
    }
?>
```

**Switch Syntax**

```php
<?php
$myNum = 2;

switch ($myNum) {
    case 1:
        echo "1";
        break;
    case 2:
        echo "2";
        break;
    case 3:
        echo "3";
        break;
    default:
        echo "None of the above";
}
?>
```

1. A switch statement is made up of the `switch` keyword, a variable to check, and a pair of curly braces `{ }`. Here we check the value of $myNum.

2. Then we have a case block for each comparison. For example case 1: echo "1"; `break`; checks whether $myNum is equal to 1. If yes, it echos "1", and uses break to exit the switch statement.
3. Otherwise, the next case block runs.

4. If all cases return `false`, the `default` case gets executed.

**Multiple Cases**

Sometimes if you have a multiple `if` expression like below, you may want to shorten it! 

```php
<?php
$myNum = 2;

if ($i == 1 ||
    $i == 2 ||
    $i == 3) {
 echo '$i is somewhere between 1 and 3.';
}
?>
```
With a `switch` statement, you can shorten the code and make your code more tidier. 

```php
<?php
case 1:
case 2:
case 3:
    echo '$i is somewhere between 1 and 3.';
    break;

?>
```

**Using "Endswitch" to END your Switch**

2 ways of creating a switch statement
```php
<?php
switch ($i) { 

}
?>
```

This can be also written in this form :
```php
<?php
switch ($i):

endswitch;
?>
```
