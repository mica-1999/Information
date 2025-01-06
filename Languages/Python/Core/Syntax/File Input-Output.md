# File Input/Output in Python

File input and output (I/O) operations are essential for many applications. Python provides built-in functions to handle file operations such as reading from and writing to files.

## Opening a File

To open a file, use the `open()` function. It requires at least one argument: the file path. You can also specify the mode in which the file should be opened.

```python
file = open('example.txt', 'r')  # Open for reading (default)
file = open('example.txt', 'w')  # Open for writing (truncates the file)
file = open('example.txt', 'a')  # Open for appending
file = open('example.txt', 'b')  # Open in binary mode
```

## Reading from a File

You can read the contents of a file using methods like `read()`, `readline()`, or `readlines()`.

```python
file = open('example.txt', 'r')
content = file.read()  # Read the entire file
line = file.readline()  # Read a single line
lines = file.readlines()  # Read all lines into a list
file.close()
```

## Writing to a File

To write data to a file, use the `write()` or `writelines()` methods.

```python
file = open('example.txt', 'w')
file.write('Hello, World!\n')  # Write a string to the file
file.writelines(['Line 1\n', 'Line 2\n'])  # Write a list of strings
file.close()
```

## Using `with` Statement

Using the `with` statement is a best practice as it ensures the file is properly closed after its suite finishes.

```python
with open('example.txt', 'r') as file:
    content = file.read()

with open('example.txt', 'w') as file:
    file.write('Hello, World!\n')
```

## File Modes

- `'r'`: Read (default)
- `'w'`: Write (truncates the file)
- `'a'`: Append
- `'b'`: Binary mode
- `'t'`: Text mode (default)
- `'+'`: Update (read and write)

## Example

```python
# Reading from a file
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)

# Writing to a file
with open('example.txt', 'w') as file:
    file.write('Hello, World!\n')
```

By understanding these basic file I/O operations, you can effectively manage files in your Python applications.