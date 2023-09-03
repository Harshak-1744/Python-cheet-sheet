# Python Baisc Concepts

## What is python?  

Python is a high-level, interpreted, and general-purpose programming language, known for its Simplicity Created by Guido Van Russom 

## Variables

In Python, variables are used to store data values. These values can be of various types, such as numbers, text, or more complex structures.

```python
# Example of variable assignment
name = "John"
age = 30
```

## Input Statement:

#### The `input()` function is used to accept user input from the keyboard. It reads a line of text from the user and returns it as a string.

**Syntax:**
```python
variable = input("Prompt message: ")
```

**Example:**
```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```
```
Enter your name: Alice!
Hello, Alice!
```
In this example, the `input()` function is used to get the user's name, and it's stored in the `name` variable.

## Output Statement:

#### The `print()` function is used to display output to the console. You can pass one or more values to `print()`, and it will convert them to strings and display them.

**Syntax:**
```python
print(value1, value2, ...)
```

**Example:**
```python
print("Hello, World!")
```
```Output:
Hello, World!
```
You can also use string formatting to display variables within a string using placeholders:

```python
name = "Alice"
age = 30
print("My name is {} and I am {} years old.".format(name, age))
```

Or, using f-strings (available in Python 3.6 and later):

```python
name = "Alice"
age = 30
print(f"My name is {name} and I am {age} years old.")
```
```Output:
My name is Alice and I am 30 years old.
```
## Data Types

In Python, data types can be broadly categorized into three main groups: primitive data types, collection data types, and user-defined data types.

### Primitive Data Types:
#### These are the most basic data types in Python and are often referred to as "primitive" 

1. **int (Integer):** Represents whole numbers, both positive and negative.

   ```python
   # Example of int
   age = 30
   ```

2. **float (Floating-Point):** Represents real numbers with a decimal point.

   ```python
   # Example of float
   pi = 3.14
   ```

3. **str (String):** Represents sequences of characters, such as text.

   ```python
   # Example of str
   message = "Hello, World!"
   ```

4. **bool (Boolean):** Represents two values - `True` or `False`. Used for logical operations.

   ```python
   # Example of bool
   is_valid = True
   ```

### Collection Data Types:
#### These data types are called "collection" data types because they can hold multiple values and are often used for grouping and organizing data.

1. **list:** An ordered collection that can contain elements of different data types.

   ```python
   # Example of list
   fruits = ["apple", "banana", "cherry"]
   ```

2. **tuple:** An ordered and immutable (unchangeable) collection of elements.

   ```python
   # Example of tuple
   coordinates = (3, 4)
   ```

3. **set:** An unordered collection of unique elements.

   ```python
   # Example of set
   unique_numbers = {1, 2, 3, 4, 5}
   ```

4. **dict (dictionary):** An unordered collection of key-value pairs.

   ```python
   # Example of dict
   person = {"name": "John", "age": 30}
   ```

### User-Defined Data Types:
#### User-defined data types are created by the programmer as custom data structures. They are not built into the language but are defined using classes and objects

1. **Class:** A blueprint for creating objects with attributes and methods.

   ```python
   # Example of a user-defined class
   class Person:
       def __init__(self, name, age):
           self.name = name
           self.age = age

   # Creating an object of the class
   person1 = Person("Alice", 25)
   ```

2. **Enumeration:** Python provides an `Enum` class for creating enumeration data types, which are a set of symbolic names (members) bound to unique values.

    ```python
    # Example of an enumeration
    from enum import Enum

    class Days(Enum):
        MONDAY = 1
        TUESDAY = 2
        WEDNESDAY = 3

    # Accessing an enumeration member
    today = Days.WEDNESDAY
    ```


## Operators

#### Operators in Python are symbols that are used to perform operations on variables and values.

### Arithmetic Operators:

#### Arithmetic operators are used for mathematical calculations.

- `+` (Addition)
- `-` (Subtraction)
- `*` (Multiplication)
- `/` (Division)
- `%` (Modulus)
- `**` (Exponentiation)

**Examples:**

```python
a = 5
b = 2

addition_result = a + b  # 5 + 2 = 7
subtraction_result = a - b  # 5 - 2 = 3
multiplication_result = a * b  # 5 * 2 = 10
division_result = a / b  # 5 / 2 = 2.5
modulus_result = a % b  # 5 % 2 = 1
exponentiation_result = a ** b  # 5 ** 2 = 25
```

### Comparison Operators:

#### Comparison operators are used to compare two values or expressions.

- `==` (Equal to): Checks if two operands are equal.
- `!=` (Not equal to): Checks if two operands are not equal.
- `<` (Less than): Checks if the left operand is less than the right operand.
- `>` (Greater than): Checks if the left operand is greater than the right operand.
- `<=` (Less than or equal to): Checks if the left operand is less than or equal to the right operand.
- `>=` (Greater than or equal to): Checks if the left operand is greater than or equal to the right operand.

**Examples:**

```python
x = 5
y = 3

equal_result = x == y  # False
not_equal_result = x != y  # True
less_than_result = x < y  # False
greater_than_result = x > y  # True
less_than_or_equal_result = x <= y  # False
greater_than_or_equal_result = x >= y  # True
```

### Logical Operators:

#### Logical operators are used to combine conditional statements.

- `and` (Logical AND): Returns True if both operands are True.
- `or` (Logical OR): Returns True if both operands are True.
- `not` (Logical NOT): Returns the opposite of the operand's truth value.

**Examples:**

```python
p = True
q = False

and_result = p and q  # False
or_result = p or q  # True
not_result = not p  # False
```

### Identity Operators:

#### Identity operators are used to compare the memory location (identity) of two objects.

- `is` (Identity operator): Returns True if both operands are the same object.
- `is not` (Negation of identity operator): Returns True if both operands are different objects.

**Examples:**

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

is_result = a is b  # True (a and b reference the same object)
is_not_result = a is not c  # True (a and c reference different objects)
```

### Membership Operators:

#### Membership operators are used to test if a sequence (such as a string, list, or tuple) contains a specific value.

- `in` (Membership operator): Returns True if a value is found in the sequence.
- `not in` (Negation of membership operator): Returns True if a value is not found in the sequence.

**Examples:**

```python
fruits = ["apple", "banana", "cherry"]

in_result = "banana" in fruits  # True
not_in_result = "orange" not in fruits  # True
```

### Bitwise Operators (Bit-level operations):

#### Bitwise operators perform operations at the bit level of binary representations.

- `&` (Bitwise AND): Performs a bitwise AND operation.
- `|` (Bitwise OR): Performs a bitwise OR operation.
- `^` (Bitwise XOR): Performs a bitwise XOR (exclusive OR) operation.
- `~` (Bitwise NOT): Performs a bitwise NOT operation, inverting all bits.
- `<<` (Left Shift): Shifts the bits of the left operand to the left by a specified number of positions.
- `>>` (Right Shift): Shifts the bits of the left operand to the right by a specified number of positions.

**Examples:**

```python
x = 5  # 0101 in binary
y = 3  # 0011 in binary

bitwise_and_result = x & y  # 0101 & 0011 = 0001 (1 in decimal)
bitwise_or_result = x | y  # 0101 | 0011 = 0111 (7 in decimal)
bitwise_xor_result = x ^ y  # 0101 ^ 0011 = 0110 (6 in decimal)
bitwise_not_result = ~x  # ~0101 = 1010 (-6 in decimal, using two's complement)
left_shift_result = x << 2  # 0101 << 2 = 010100 (20 in decimal)
right_shift_result = x >> 2  # 0101 >> 2 = 0001 (1 in decimal)
```
## Control Structures
Control structures allow you to control the flow of your program.

### Conditional Statements 
Conditional statements are used for decision-making.

- `if` Statement
- `else` Statement
- `elif` Statement
- `nested if` Statement

### 1. `if` Statement:

#### The `if` statement is used to execute a block of code if a specified condition is `True`.

**Syntax:**
```python
if condition:
    # block of code
```

**Example:**
```python
x = 10

if x > 5:
    print("x is greater than 5")
```

### 2. `elif` Statement:

#### The `elif` statement (short for "else if") is used to check multiple conditions one by one. If the previous `if` or `elif` conditions are `False`, it tests the current condition.

**Syntax:**
```python
if condition1:
    # Code to execute if condition1 is True
elif condition2:
    # Code to execute if condition2 is True (if condition1 is False)
```

**Example:**
```python
x = 10

if x > 15:
    print("x is greater than 15")
elif x > 5:
    print("x is greater than 5 but not greater than 15")
```

### 3. `else` Statement:

#### The `else` statement is used to execute a block of code if the preceding `if` and `elif` conditions are `False`.

**Syntax:**
```python
if condition:
    # Code to execute if the condition is True
else:
    # Code to execute if the condition is False
```

**Example:**
```python
x = 3

if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```

### 4. Nested `if` Statements:

####  Nested `if` statements are `if` statements placed inside another `if` or `elif` block. They allow you to test conditions within conditions.

**Syntax:**
```python
if condition1:
    # Code for condition1
    if condition2:
        # Code for condition2 inside condition1
    else:
        # Code if condition2 is not met inside condition1
else:
    # Code if condition1 is not met
```

**Example:**
```python
x = 10

if x > 5:
    print("x is greater than 5")
    if x < 15:
        print("x is less than 15 inside the first if")
    else:
        print("x is not less than 15 inside the first if")
else:
    print("x is not greater than 5")
```

### Loops 

Loops are used to repeat a block of code multiple times.



### 1. `for` Loop:

#### The `for` loop is used to iterate over elements of an iterable (like a list, tuple, or range) and execute a block of code for each element.

**Syntax:**
```python
for variable in iterable:
    # Code to repeat for each item in the iterable
```

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

**Solution:**
```
apple
banana
cherry
```

This `for` loop iterates over the `fruits` list and prints each fruit name on a separate line.


```python
count = 0

while count < 5:
    print(count)
    count += 1
```

### 2. `while` Loop:

#### The `while` loop repeatedly executes a block of code as long as a specified condition is `True`.

**Syntax:**
```python
while condition:
    # Code to repeat as long as the condition is True
```

**Example:**
```python
count = 0

while count < 5:
    print(count)
    count += 1
```
**Solution:**
```
0
1
2
3
4
```
This `while` loop initializes a `count` variable to 0 and repeatedly prints its value as long as `count` is less than 5. It increments `count` by 1 in each iteration.

### 1. `break` Statement:

#### The `break` statement is used to exit a loop prematurely when a certain condition is met. It allows you to terminate the loop before it has completed all iterations.

**Syntax:**
```python
for variable in iterable:
    # Code
    if some_condition:
        break
```

**Example:**
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

**Solution:**
```
0
1
2
3
4
```

In this example, the `break` statement is encountered when `i` is equal to 5. It exits the loop immediately, and the remaining iterations are skipped.

### 2. `continue` Statement:

#### The `continue` statement is used to skip the current iteration of a loop and continue to the next iteration. It allows you to bypass the rest of the code within the loop for the current iteration.

**Syntax:**
```python
for variable in iterable:
    # Code
    if some_condition:
        continue
    # More code
```

**Example:**
```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

**Solution:**
```
0
1
3
4
```

In this example, when `i` is equal to 2, the `continue` statement is encountered. It skips the `print(i)` statement for that iteration and proceeds to the next iteration.

### 3. `pass` Statement:

#### The `pass` statement is a placeholder that does nothing. It is used when syntactically a statement is required, but no action is desired or required. It is often used as a placeholder for future code.

**Syntax:**
```python
if some_condition:
    pass
```

**Example:**
```python
for i in range(3):
    if i == 1:
        pass
    else:
        print(i)
```

**Solution:**
```
0
2
```

In this example, when `i` is equal to 1, the `pass` statement is encountered, and it does nothing. For other values of `i`, it prints the value as specified in the `else` block.

