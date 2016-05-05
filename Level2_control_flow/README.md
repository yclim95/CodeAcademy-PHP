# Level2_control_flow

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