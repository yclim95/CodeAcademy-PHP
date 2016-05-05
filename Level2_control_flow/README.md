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
