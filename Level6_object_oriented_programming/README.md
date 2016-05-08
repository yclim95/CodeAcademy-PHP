#Level 6 Object Oriented Programming (OOP)
## What is Object-Oriented Programming (OOP)? 
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

Al'right at this point you should understand what is a properties. 

But now we have an issue. 

`$teacher` and `$student` are the same, which should be changed immediately, correct? :

*Solutions* :

```php
<?php
public function __construct($prop1, $prop2) {
  $this->prop1 = $prop1;
  $this->prop2 = $prop2;
}
?>
```
**Note** : *Public keyowrd and the arrow notation*

1. You're creating a function bound to a class (a **method**).

2. The constructor method has to be called `__construct()`.

3. Finally, the weird way to assign the values: `$this->prop1 = $prop1` means that the value you pass in the `__construct()` function via the new keyword is assigned to $this, which represents the object you are dealing with, and `->prop1` is the actual property of the object.

4. By creating a `new` instance using the new keyword, you actually call this` __construct()` method, which constructs the object. And that's why we have to pass in some arguments when we create an instance of a class, since this is how the properties get set!

### 3. Methods 

```php
<?php
public function funcname($optionalParameter) {
  // Do something
}
?>
```

If we want a method to return a sentence containing the firstname, we would have to use `$this->firstname`. (As you see, there is no $ when you access a property in a class.)

Calling a method is similar to accessing a property, you just have to add the parentheses:

```php
<?php
$obj1 -> meth1();
?>
```

## Class & Object Methods 
### 1. Is_a() 
Used to find out if a particular object is an **instance** of a given class

```php
<?php
	if (is_a($me, "Person")) {
		echo "I'm a person, ";
	}
?>
```

### 2. Property_exists()
To see if an object has a given **property**

```php
<?php
	if (property_exists($me, "name")) {
		echo "I have a name, ";
	}
?>
```

### 3. Method_exists() 
To see if an object has a given **method**

```php
<?php
	if (method_exists($me, "dance")) {
		echo "and I know how to dance!";
	}
?>
```

## OOP Concepts 
### 1. Inheritance 
As you've been thinking about classes and objects, you might have realized that one class might actually be a specialized type of another class. For instance, you might have a `Vehicle` class and a `Truck` class, and it would probably save you an awful lot of typing if you could somehow specify that `Truck` instances should automatically have many of the same properties and methods as `Vehicle` instances.

PHP allows us to accomplish this through a process called **inheritance**. **Inheritance** is a way for one class to take on the properties or methods of another class. You could say that the one class **extends** the other. This is used to express an "*is-a*" relationship—for example, a Truck "is-a" Vehicle, so it could inherit from Vehicle, but a Motorcycle isn't a Truck, so it shouldn't inherit from Truck (though both could inherit from Vehicle).

This can be done with a keyord -> `extends`.

```php
<?php
        class Shape {
          public $hasSides = true;
        }
        
        class Square extends Shape {
        
        }
        
        $square = new Square();
        // Add your code below!
        if (property_exists($square,"hasSides")) {
          echo "I have sides!";
        }
?>
```

### 2. Overriding Methods 
Sometimes we want a child class (or **subclass**) to be able to override a property or method of its parent class (or **superclass**).

For instance, we might have a `Shape` class with a `$sides` property set to true, but we might want Square to override this property and set `$sides` to 4 (since a square always has four sides). That would look something like this:

```php
<?php
class Shape {
  $sides = true;
}

class Square extends Shape {
  $sides = 4;
}
?>
```

** Sample of overriding methods** 
```php
<?php
	class Vehicle {
		public function honk() {
			return "HONK HONK!";
		}
	}
	// Add your code below!
	class Bicycle extends Vehicle{
		public function honk(){
			return "Beep beep!";   
		}
	}

	$bicycle = new Bicycle();
	echo $bicycle->honk();
?>
```

## PHP OOP Keywords
### 1. Final Keyword 
In PHP, a parent class can prevent its methods from being overridden by its children with—you guessed it—the `final` keyword.

You'd want to use the `final` keyword in your code to *control* what methods can be modified by a class' **subclasses**. For instance, you might want all `Vehicles` to have the same `drive()` method no matter what, so you would prefix its method definition with `final`, like so:

```php
<?php
class Vehicle {
  final public function drive() {
    return "I'm drivin' here!";
  }
}
?>
```

### 2. Const Keyword
Sometimes we want variables that don't change. These are prefixed with the const keyword (short for **constant**).

PHP lets us set constants on a class-by-class basis! Each class has its own **scope**, which is the context in which its variables can be used.

```php
<?php
class Immortal extends Person {
  // Immortals never die!
  const alive = true;
}

// If true...
if (Immortal::alive) {
  echo "I live forever!";
}
// echoes "I live forever!"
?>
```

In the example above, we use `::` to access the `alive` constant inside the `Immortal` class.

**Note**: that `const`ants do not start with `$`

### 3. Static Keyword
You might be wondering whether it's possible to access class properties or methods without creating an instance of the class. 
*The answer: Yes!*

** How ? ** 
By using the keywords `static`.
Lets you use a class' property or method without having to create an instance of that class. It works like this:

```php
<?php
class Person {
  public static $isAlive = "Yep!"
  public static function greet() {
    echo "Hello there!";
  }
}

echo Person::$isAlive;
// prints "Yep!"
Person::greet();
// prints "Hello there!"
?>
```

### 3. Static + Cost using Scope Resoulution Operator (::)

```php
<?php
	class Person {
		static public function say(){
			echo "Here are my thoughts!";   
		}
	}

	class Blogger extends Person{
		const cats = 50; 
	}

	echo Blogger::cats;
	echo Person::say();
?>
```