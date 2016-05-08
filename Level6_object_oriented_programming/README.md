#Level6_object_oriented_programming
## What is Object-Oriented Programming ? 
PHP is an object-oriented programming language, which means that you can create objects, which can contain variables and functions.

When talking about **objects**, you refer to variables belonging to these objects as **properties** (or attributes or fields), and functions are called methods.

These objects are essential when dealing with PHP, as almost everything is an object: for example, functions or arrays are objects, too!
And this shows why we use objects: we can bundle our functions and data in one place, we can create objects easily using classes (object constructors), so we can create lots of instances (objects, which have been constructed via a class), which contain mostly the same data, except some little nuances.

On the right, there is a Person **class** and one **instance** stored in $me on line 32. Then the greet() method of the $me object is called and the result is echod on line 35.

## Objects in Real Life
Every forum user (object) has the same rights: he can log in and write (methods), can contain some settings (properties), but every user has a different name (another property).

Every user is created easily, as you create a new instance of a User class when you sign up. And as we've seen, there are some properties and methods that every instance has in common (such as logging in and writing), and there are some which are unique (such as each user's name).

And without object-oriented programming—OOP for short—this could not be done that easily.

Another example: on the right, there is a `Person` class, so every new Person has some properties, like `$isAlive` or `$firstname`, and a method `greet()`.

Right now there is only one instance of the `Person` class: `$me`. But we'll reconstruct this class and you'll even create another instance of the class, so your name will be echod, too.

```php
<?php
 // The code below creates the class
        class Person {
            // Creating some properties (variables tied to an object)
            public $isAlive = true;
            public $firstname;
            public $lastname;
            public $age;
            
            // Assigning the values
            public function __construct($firstname, $lastname, $age) {
              $this->firstname = $firstname;
              $this->lastname = $lastname;
              $this->age = $age;
            }
            
            // Creating a method (function tied to an object)
            public function greet() {
              return "Hello, my name is " . $this->firstname . " " . $this->lastname . ". Nice to meet you! :-)";
            }
          }
          
        // Creating a new person called "boring 12345", who is 12345 years old ;-)
        $me = new Person('boring', '12345', 12345);
        
        // Printing out, what the greet method returns
        echo $me->greet(); 
?>
```

## Classes Syntax 
### 1. Classes 
```php
<?php
class Classname {

}
?>
```

### 2. Properties 

```php
<?php
class Fruit {
  public $count = 3;
  public $type;
}

$apple = new Fruit();
$apple->type = "apple";
print $apple->count; // 3
print $apple->type;  // apple
?>
```