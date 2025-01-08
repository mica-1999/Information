# PHP Object-Oriented Programming (OOP)

## Introduction

Object-oriented programming (OOP) in PHP allows you to create reusable and modular code by organizing it into classes and objects. OOP concepts include classes, objects, inheritance, polymorphism, and encapsulation.

## Classes and Objects

### Defining a Class

A class is defined using the `class` keyword followed by the class name.

### Example

```php
<?php
class Person {
  public $name;
  public $age;

  public function __construct($name, $age) {
    $this->name = $name;
    $this->age = $age;
  }

  public function greet() {
    return "Hello, my name is $this->name and I am $this->age years old.";
  }
}
?>
```

### Creating an Object

An object is an instance of a class, created using the `new` keyword.

### Example

```php
<?php
$person = new Person("John Doe", 30);
echo $person->greet();
?>
```

## Inheritance

Inheritance allows a class to inherit properties and methods from another class.

### Example

```php
<?php
class Employee extends Person {
  public $jobTitle;

  public function __construct($name, $age, $jobTitle) {
    parent::__construct($name, $age);
    $this->jobTitle = $jobTitle;
  }

  public function getJobTitle() {
    return $this->jobTitle;
  }
}

$employee = new Employee("Jane Smith", 25, "Software Engineer");
echo $employee->greet();
echo " Job Title: " . $employee->getJobTitle();
?>
```

## Polymorphism

Polymorphism allows objects of different classes to be treated as objects of a common superclass. It is achieved through method overriding.

### Example

```php
<?php
class Animal {
  public function makeSound() {
    return "Some sound";
  }
}

class Dog extends Animal {
  public function makeSound() {
    return "Bark";
  }
}

class Cat extends Animal {
  public function makeSound() {
    return "Meow";
  }
}

$dog = new Dog();
$cat = new Cat();
echo $dog->makeSound(); // Output: Bark
echo $cat->makeSound(); // Output: Meow
?>
```

## Encapsulation

Encapsulation is the concept of restricting access to certain properties and methods of an object. It is achieved using access modifiers: `public`, `protected`, and `private`.

### Example

```php
<?php
class BankAccount {
  private $balance;

  public function __construct($balance) {
    $this->balance = $balance;
  }

  public function deposit($amount) {
    $this->balance += $amount;
  }

  public function withdraw($amount) {
    if ($amount <= $this->balance) {
      $this->balance -= $amount;
    } else {
      echo "Insufficient funds";
    }
  }

  public function getBalance() {
    return $this->balance;
  }
}

$account = new BankAccount(1000);
$account->deposit(500);
$account->withdraw(300);
echo "Balance: " . $account->getBalance(); // Output: Balance: 1200
?>
```

## Example

Combining different OOP concepts to create a simple program.

```php
<?php
class Person {
  public $name;
  public $age;

  public function __construct($name, $age) {
    $this->name = $name;
    $this->age = $age;
  }

  public function greet() {
    return "Hello, my name is $this->name and I am $this->age years old.";
  }
}

class Employee extends Person {
  public $jobTitle;

  public function __construct($name, $age, $jobTitle) {
    parent::__construct($name, $age);
    $this->jobTitle = $jobTitle;
  }

  public function getJobTitle() {
    return $this->jobTitle;
  }
}

$employee = new Employee("Jane Smith", 25, "Software Engineer");
echo $employee->greet();
echo " Job Title: " . $employee->getJobTitle();
?>
