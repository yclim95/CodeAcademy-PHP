# Level3_arrays
## 1. What is an Array ?

An array is a list of items, a bit like a shopping list. It allows you to store more than one item in only one variable.

Think of it like this. When writing your shopping list, you could use a separate piece of paper for each item you need to buy (a variable). However this is silly and unneeded—could you imagine how hard it would be to carry all that paper around with you? So, you use one piece of paper for all of your items. This one piece of paper is your array.

E.G :
```php
<?php
$array = array("Egg", "Tomato", "Beans");
?>
```

## 2. Array Syntax

Have you noticed something familiar at the start of our array? That's right, it starts in the same way as a variable, with the `$` sign, and then a name, followed by `=`.

However, this is when things start to get different. When declaring an array, we have to use `array()`. This basically tells PHP that $array is an array and not something else, such as a regular old variable.

By now, I am sure you have noticed the text inside the ( and ). This is just the items in our array. So, currently, our array has the items "Egg," "Tomato," and "Beans" in it. You can add any type of information to an array, and you do it in much the same way as when declaring variables. Use "" when adding strings, and just enter the number when adding integers.

You must always remember, however, that each item in an array must be separated by a comma: `,`.

3. Access arrays by offsets []

Each item in an array is numbered starting from 0. For example, when we create an array:

```php
<?php
$myArray = array("do", "re", "mi");
?>
```
Each item is numbered starting from 0, like this:
 

| "Do"        | "Re"           | "Mi"  |
| ------------- |:-------------:| -----:|
| 0     | 1 | 2 |


The item `"do"` is in position 0, the item `"re"` is in position 1, and so on.

Therefore, we can access a particular item of the array using its position, like this:

```php
<?php
$myArray = array("do", "re", "mi");

echo $myArray[0]
// outputs "do"
?>

1. First we create an array named $myArray

2. Then we use `echo` to output the first item in $myArray. Since items are numbered starting from 0, "do" is at position 0.
```

**Array can also be access by offset {}

```php
<?php
$myArray = array("do", "re", "mi");
 print $myArray{2};
 // prints "mi";
?>