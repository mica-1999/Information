# Control Flow in Python

## Introduction

Control flow statements in Python allow you to control the execution of your code based on certain conditions and loops. These statements include conditional statements, loops, and control flow tools.

## Conditional Statements

### if Statement

The `if` statement is used to test a condition. If the condition is true, the block of code inside the `if` statement is executed.

```python
x = 10
if x > 5:
    print("x is greater than 5")
```

### if-else Statement

The `if-else` statement provides an alternative block of code that is executed if the condition is false.

```python
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```

### if-elif-else Statement

The `if-elif-else` statement allows you to test multiple conditions.

```python
x = 10
if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but less than or equal to 15")
else:
    print("x is 5 or less")
```

## Loops

### for Loop

The `for` loop is used to iterate over a sequence (such as a list, tuple, or string).

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

### while Loop

The `while` loop is used to execute a block of code as long as a condition is true.

```python
i = 1
while i < 6:
    print(i)
    i += 1
```

## Control Flow Tools

### break Statement

The `break` statement is used to exit a loop prematurely.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### continue Statement

The `continue` statement is used to skip the current iteration of a loop and continue with the next iteration.

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)
```

### pass Statement

The `pass` statement is a null operation; it is used when a statement is required syntactically but you do not want any command or code to execute.

```python
for i in range(10):
    if i % 2 == 0:
        pass
    else:
        print(i)
```

## Example

Combining control flow statements to create a simple program.

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    if number % 2 == 0:
        print(f"{number} is even")
    else:
        print(f"{number} is odd")
