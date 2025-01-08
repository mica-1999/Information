# PHP Arrays

## Introduction

Arrays in PHP are used to store multiple values in a single variable. They are a fundamental data structure in PHP and are used to organize and manipulate data.

## Types of Arrays

### Indexed Arrays

Indexed arrays store a series of values with numeric keys.

### Example

```php
<?php
$fruits = array("Apple", "Banana", "Cherry");
echo $fruits[0]; // Output: Apple
?>
```

### Associative Arrays

Associative arrays store values with named keys.

### Example

```php
<?php
$person = array("name" => "John Doe", "age" => 30);
echo $person["name"]; // Output: John Doe
?>
```

### Multidimensional Arrays

Multidimensional arrays contain one or more arrays.

### Example

```php
<?php
$people = array(
  array("name" => "John Doe", "age" => 30),
  array("name" => "Jane Smith", "age" => 25)
);
echo $people[0]["name"]; // Output: John Doe
?>
```

## Array Functions

PHP provides various functions to manipulate arrays.

### count()

The `count()` function returns the number of elements in an array.

### Example

```php
<?php
$fruits = array("Apple", "Banana", "Cherry");
echo count($fruits); // Output: 3
?>
```

### array_push()

The `array_push()` function adds one or more elements to the end of an array.

### Example

```php
<?php
$fruits = array("Apple", "Banana");
array_push($fruits, "Cherry");
print_r($fruits); // Output: Array ( [0] => Apple [1] => Banana [2] => Cherry )
?>
```

### array_pop()

The `array_pop()` function removes the last element from an array.

### Example

```php
<?php
$fruits = array("Apple", "Banana", "Cherry");
array_pop($fruits);
print_r($fruits); // Output: Array ( [0] => Apple [1] => Banana )
?>
```

### array_merge()

The `array_merge()` function merges one or more arrays.

### Example

```php
<?php
$array1 = array("Apple", "Banana");
$array2 = array("Cherry", "Date");
$result = array_merge($array1, $array2);
print_r($result); // Output: Array ( [0] => Apple [1] => Banana [2] => Cherry [3] => Date )
?>
```

## Example

Combining different array concepts to create a simple program.

```php
<?php
$fruits = array("Apple", "Banana", "Cherry");
$person = array("name" => "John Doe", "age" => 30);
$people = array(
  array("name" => "John Doe", "age" => 30),
  array("name" => "Jane Smith", "age" => 25)
);

echo "Number of fruits: " . count($fruits) . "<br>";
array_push($fruits, "Date");
echo "Fruits: ";
print_r($fruits);
echo "<br>";

array_pop($fruits);
echo "Fruits after pop: ";
print_r($fruits);
echo "<br>";

echo "Person's name: " . $person["name"] . "<br>";
echo "First person's name: " . $people[0]["name"] . "<br>";
?>
