## 1. String Basics

### Definition
A string is a sequence of characters enclosed in single quotes (''), double quotes (" "), or triple quotes (''' ''''). It is an immutable data type in Python.

### Creating Strings
```python
single_quoted = 'This is a single-quoted string'
double_quoted = "This is a double-quoted string"
triple_quoted = '''This is a triple-quoted string'''
```

## 2. String Operations

### Concatenation
Strings can be concatenated using the `+` operator.
```python
str1 = "Hello"
str2 = "World"
result = str1 + ", " + str2
print(result)  # Output: Hello, World
```

### String Repetition
Strings can be repeated using the `*` operator.
```python
str1 = "Python "
result = str1 * 3
print(result)  # Output: Python Python Python
```

## 3. String Methods

### `upper()` and `lower()`
Converts a string to uppercase or lowercase.
```python
text = "Hello, World"
uppercase_text = text.upper()
lowercase_text = text.lower()
print(uppercase_text)  # Output: HELLO, WORLD
print(lowercase_text)  # Output: hello, world
```

### `strip()`
Removes leading and trailing whitespace characters.
```python
text = "   Python   "
stripped_text = text.strip()
print(stripped_text)  # Output: "Python"
```

### `replace()`
Replaces a substring with another substring.
```python
text = "I like apples"
new_text = text.replace("apples", "bananas")
print(new_text)  # Output: "I like bananas"
```

### `split()`
Splits a string into a list of substrings based on a delimiter.
```python
text = "apple,banana,cherry"
fruits = text.split(",")
print(fruits)  # Output: ['apple', 'banana', 'cherry']
```

## 4. String Formatting

### `format()` Method
Formats strings by replacing placeholders with values.
```python
name = "Alice"
age = 30
message = "My name is {} and I am {} years old.".format(name, age)
print(message)  # Output: "My name is Alice and I am 30 years old."
```

### F-Strings (Formatted String Literals)
A more concise way to format strings using f-strings.
```python
name = "Bob"
age = 25
message = f"My name is {name} and I am {age} years old."
print(message)  # Output: "My name is Bob and I am 25 years old."
```
