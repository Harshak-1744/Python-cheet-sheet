# File Handling in Python
 
File handling in Python allows you to work with files, such as reading from them, writing to them, and modifying their content. In this guide, we'll cover the basics with easy-to-understand examples.

## Opening a File

To work with a file, you first need to open it. You can use the `open()` function for this purpose. Here's how to do it:

```python
# Opening a file for reading
file = open("sample.txt", "r")
```

- `"sample.txt"` is the name of the file we want to open.
- `"r"` specifies that we want to open the file in **read mode**.

## Reading from a File

Once the file is open, you can read its contents using methods like `read()`. Here's an example:

```python
# Reading the entire file
content = file.read()
print(content)
```

When you run this code:
- It opens the "sample.txt" file and reads its entire content.
- The content of the file is then printed to the console.

## Closing a File

After you're done with a file, it's important to close it using `close()` to free up system resources:

```python
file.close()
```

Failing to close a file can cause issues in your program and can lead to data loss.

## Writing to a File

To write data to a file, you can open it in **write mode** using `"w"` as the mode:

```python
# Opening a file for writing
file = open("output.txt", "w")

# Writing to the file
file.write("Hello, World!")

# Closing the file
file.close()
```

When you run this code:
- It opens the "output.txt" file in write mode.
- It writes the text "Hello, World!" into the file.
- The file is then closed.

## Appending to a File

If you want to add content to an existing file without overwriting its current content, you can open it in **append mode** using `"a"`:

```python
# Opening a file for appending
file = open("output.txt", "a")

# Appending to the file
file.write("\nAppending new data!")

# Closing the file
file.close()
```

When you run this code:
- It opens the "output.txt" file in append mode.
- It appends the text "Appending new data!" to the end of the file.
- The file is then closed.

## Using `with` Statement

Python provides a convenient way to open and work with files using the `with` statement. It ensures that the file is properly closed when you're done:

```
# Using 'with' to open a file
with open("sample.txt", "r") as file:
    content = file.read()
    print(content)

# File is automatically closed when 'with' block is exited
```

With this code:
- The "sample.txt" file is opened in read mode within the `with` block.
- The content is read and printed.
- The file is automatically closed when the block is exited.


# Example 
```
# Example Python snippet for writing to a file

# List of strings to be written to file
lines_to_write = ["Hello, world!", "This is an example.", "Writing to a file in Python."]

# Open a file in write mode
with open('output.txt', 'w') as file:
    # Write each string in the list to the file
    for line in lines_to_write:
        file.write(line + '\n')

# File is automatically closed after the 'with' block
```

