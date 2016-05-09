#Level 7 Advanced Array
## Associative Arrays 
So far, you have been accessing the values of an array using integers. This is all well and good, but if you want to be more descriptive of your data, you can make use of something called an **associative array**.

An **associative array** makes use of (`key => value`) pairs. Some languages may separate arrays from associative arrays, but PHP treats both as the same.

```php
<?php
        // This is an array using integers as the indices...
        $myArray = array(2012, 'blue', 5);

        // ...and this is an associative array:
        $myAssocArray = array('year' => 2012,
                        'colour' => 'blue',
                        'doors' => 5);
            
        // This code will output "blue"...
        echo $myArray[1];
        echo '<br />';
            
        // ... and this will also output "blue"!
        echo $myAssocArray['colour'];
?>
```

### 1. Using Arrays as Maps

You can think of an associative array (also called a **map**) as being the same as a normal array, but instead of using an integer to refer to the value, you use a defined key.

### 2. Accessing Associative Arrays 
```php
<?php
  echo 'I have a ' . $myAssocArray ['year'] . ' ' . $myAssocArray ['make'] . '. It is ' . $myAssocArray ['colour'] . ' and has ' . $myAssocArray ['doors'] . ' doors.';

?>
```

### 3. Iterating over Associative Arrays 
```php
<?php
        $food = array('pizza', 'salad', 'burger');
        $salad = array('lettuce' => 'with',
                   'tomato' => 'without',
                   'onions' => 'with');
    
      // Looping through an array using "for".
      // First, let's get the length of the array!
      $length = count($food);
    
      // Remember, arrays in PHP are zero-based:
      for ($i = 0; $i < $length; $i++) {
        echo $food[$i] . '<br />';
      }
    
      echo '<br /><br />I want my salad:<br />';
    
      // Loop through an associative array using "foreach":
      foreach ($salad as $ingredient=>$include) {
        echo $include . ' ' . $ingredient . '<br />';
      }

      // I want my salad:
      // with lettuce 
      // without tomato 
      // with onions 
    
      echo '<br /><br />';
?>
```

### 4. Multi-Dimensional Array 
Not only can you store integers and strings in arrays, you can also store... other arrays! This is called a **multidimensional array**.

How do we do this? Well, just like a normal array with comma-separated values, but you would put comma-separated arrays instead—just like the code in the editor.

`$deck` is an array which contains 3 rows, each being a playing card. Within each row, it has the name of the card, along with the value.

To retrieve a card, we would first get the row for that card, then get the value we require (either to display the card, or calculate the player's total).

If we access `$deck[2]`, we would get the third row (remember, arrays start from 0 in PHP!)

That will return another array containing 2 values: the first (0) which is a string that has the value "7 of Diamonds", and the second (1) which is an integer that has the value 7.

If we want the "7 of Diamonds" string, we would simply use `$deck[2][0]`;.