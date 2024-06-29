Day 2: Types in Python
======================

Morning
-------

### Reflection from Last Day:
* Answer questions about Chapter 1 of CLRS
* Finish Chapter 1 exercises (1.1-1 up to 1.1-5. 1.2-1 up to 1.2-3. 1-1)


### Integers (`int`):
Integers are whole numbers, without a fractional component.

```python
# Positive integer
a = 10

# Negative integer
b = -5

# Zero
c = 0
```

### Floating-Point Numbers (`float`):
Floating-point numbers have a decimal point and can represent fractional values.

```python
# Positive float
d = 10.5

# Negative float
e = -3.14

# Zero as a float
f = 0.0

# Scientific notation
g = 1.23e4  # This is equal to 12300.0
h = 1.23e-4  # This is equal to 0.000123
```

### Complex Numbers (`complex`):
Complex numbers have a real and an imaginary part, represented as `a + bj`, where `a` is the real part and `b` is the imaginary part.

```python
# Complex number with real and imaginary parts
i = 2 + 3j

# Complex number with only a real part
j = 5 + 0j

# Complex number with only an imaginary part
k = 0 + 7j
```

Try these on your computer!

In Python, strings are sequences of characters enclosed in either single quotes (`'`), double quotes (`"`), triple single quotes (`'''`), or triple double quotes (`"""`). Here are some examples demonstrating the different ways to work with strings:

### Basic String Creation
```python
# Single quotes
a = 'Hello, World!'
print(a)  # Output: Hello, World!

# Double quotes
b = "Hello, World!"
print(b)  # Output: Hello, World!

# Triple single quotes (for multi-line strings)
c = '''Hello,
World!'''
print(c)
# Output:
# Hello,
# World!

# Triple double quotes (for multi-line strings)
d = """Hello,
World!"""
print(d)
# Output:
# Hello,
# World!
```

### String Concatenation
```python
# Using the + operator
e = "Hello" + ", " + "World!"
print(e)  # Output: Hello, World!

# Using f-strings (formatted string literals)
name = "Alice"
f = f"Hello, {name}!"
print(f)  # Output: Hello, Alice!

# Using the join method
g = " ".join(["Hello", "World!"])
print(g)  # Output: Hello World!
```

### String Repetition
```python
# Repeating a string multiple times
h = "Ha" * 3
print(h)  # Output: HaHaHa
```

### String Indexing and Slicing
```python
# Indexing (accessing a single character)
i = "Hello"
print(i[0])  # Output: H
print(i[-1])  # Output: o

# Slicing (accessing a substring)
j = "Hello, World!"
print(j[0:5])  # Output: Hello
print(j[7:])  # Output: World!
print(j[:5])  # Output: Hello
print(j[::2])  # Output: Hlo ol!
```

### String Methods
```python
# Convert to uppercase
k = "hello".upper()
print(k)  # Output: HELLO

# Convert to lowercase
l = "HELLO".lower()
print(l)  # Output: hello

# Strip whitespace
m = "  Hello  ".strip()
print(m)  # Output: Hello

# Replace substrings
n = "Hello, World!".replace("World", "Python")
print(n)  # Output: Hello, Python!

# Split into a list
o = "Hello, World!".split(", ")
print(o)  # Output: ['Hello', 'World!']

# Find a substring
p = "Hello, World!".find("World")
print(p)  # Output: 7 (index of the first occurrence of "World")
```

### String Formatting
```python
# Using the format method
q = "Hello, {}!".format("Alice")
print(q)  # Output: Hello, Alice!

# Using f-strings (formatted string literals)
r = f"Hello, {name}!"
print(r)  # Output: Hello, Alice!

# Using % operator
s = "Hello, %s!" % "Alice"
print(s)  # Output: Hello, Alice!
```

### Multiline Strings with Line Breaks
```python
# Using triple quotes
t = """This is a string
that spans multiple
lines."""
print(t)
# Output:
# This is a string
# that spans multiple
# lines.
```

These examples cover the basics of string creation, manipulation, and formatting in Python.

Here are some examples demonstrating boolean types (`bool`) in Python, including their creation, usage in logical operations, and conversion from other types:

### Basic Boolean Values
```python
# Boolean True
a = True
print(a)  # Output: True

# Boolean False
b = False
print(b)  # Output: False
```

### Boolean from Comparisons
```python
# Comparison resulting in True
c = 5 > 3
print(c)  # Output: True

# Comparison resulting in False
d = 5 < 3
print(d)  # Output: False
```

### Boolean Operations
```python
# Logical AND
e = True and False
print(e)  # Output: False

# Logical OR
f = True or False
print(f)  # Output: True

# Logical NOT
g = not True
print(g)  # Output: False
```

### Using Boolean in Conditional Statements
```python
# If statement
p = True
if p:
    print("This is True")  # Output: This is True

# If-else statement
q = False
if q:
    print("This is True")
else:
    print("This is False")  # Output: This is False
```

### Boolean Methods and Properties
```python
# Checking if a boolean is True
r = True
if r is True:
    print("r is True")  # Output: r is True

# Checking if a boolean is False
s = False
if s is False:
    print("s is False")  # Output: s is False

# Using booleans in expressions
t = 10 > 5 and 5 < 20
print(t)  # Output: True

u = not (5 == 5)
print(u)  # Output: False
```

These examples demonstrate the basic usage of boolean types, including their values, operations, conversions, and use in conditional statements.

In Python, `NoneType` is the type of the `None` object, which is used to represent the absence of a value or a null value. Here's an overview of `NoneType` and a simple use:

### Assigning None to a variable
```python
a = None
print(a)  # Output: None
```

### Checking if a variable is None
```python
if a is None:
    print("a is None")  # Output: a is None
else:
    print("a is not None")
```


Afternoon
---------

In Python, arrays can be created using different data structures, each with its own use cases and characteristics. Here are some common types of arrays in Python:

### Lists
Lists are the most versatile array type in Python. They can store elements of different types and support various operations.

```python
# Creating a list
a = [1, 2, 3, 4, 5]
print(a)  # Output: [1, 2, 3, 4, 5]

# Accessing elements
print(a[0])  # Output: 1
print(a[-1])  # Output: 5

# Modifying elements
a[2] = 10
print(a)  # Output: [1, 2, 10, 4, 5]

# Adding elements
a.append(6)
print(a)  # Output: [1, 2, 10, 4, 5, 6]

# Removing elements
a.remove(10)
print(a)  # Output: [1, 2, 4, 5, 6]

# Slicing
print(a[1:4])  # Output: [2, 4, 5]
```

### Tuples
Tuples are similar to lists but are immutable, meaning their elements cannot be changed after creation.

```python
# Creating a tuple
b = (1, 2, 3, 4, 5)
print(b)  # Output: (1, 2, 3, 4, 5)

# Accessing elements
print(b[0])  # Output: 1
print(b[-1])  # Output: 5

# Tuples are immutable, so elements cannot be modified
# b[2] = 10  # This will raise a TypeError

# Slicing
print(b[1:4])  # Output: (2, 3, 4)
```

### Arrays (from the `array` module)
The `array` module provides a way to create arrays with a fixed type.

```python
import array

# Creating an integer array
c = array.array('i', [1, 2, 3, 4, 5])
print(c)  # Output: array('i', [1, 2, 3, 4, 5])

# Accessing elements
print(c[0])  # Output: 1
print(c[-1])  # Output: 5

# Modifying elements
c[2] = 10
print(c)  # Output: array('i', [1, 2, 10, 4, 5])

# Adding elements
c.append(6)
print(c)  # Output: array('i', [1, 2, 10, 4, 5, 6])

# Removing elements
c.remove(10)
print(c)  # Output: array('i', [1, 2, 4, 5, 6])

# Slicing
print(c[1:4])  # Output: array('i', [2, 4, 5])
```

### Lists of Lists (2D Arrays)
Lists of lists can be used to create multi-dimensional arrays.

```python
# Creating a 2D list
f = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
print(f)
# Output:
# [[1, 2, 3],
#  [4, 5, 6],
#  [7, 8, 9]]

# Accessing elements
print(f[0][0])  # Output: 1
print(f[1][2])  # Output: 6

# Modifying elements
f[0][0] = 10
print(f)
# Output:
# [[10, 2, 3],
#  [4, 5, 6],
#  [7, 8, 9]]
```

These examples cover various array types in Python, including lists, tuples, arrays from the `array` module, NumPy arrays, and lists of lists for 2D arrays.



In Python, functions are first-class objects, meaning they can be passed around and used as arguments just like any other object (e.g., string, int, float, list, etc.). Functions in Python are instances of the `function` type, which is a built-in type. Here are examples of defining, using, and passing functions in Python:

### Defining Functions
```python
# Simple function definition
def greet(name):
    return f"Hello, {name}!"

# Calling the function
print(greet("Alice"))  # Output: Hello, Alice!
```

### Functions as First-Class Objects
```python
# Assigning a function to a variable
def add(a, b):
    return a + b

sum_function = add

# Calling the function through the variable
print(sum_function(3, 4))  # Output: 7
```

### Passing Functions as Arguments
```python
# Function that takes another function as an argument
def operate(func, x, y):
    return func(x, y)

# Using the function
result = operate(add, 5, 3)
print(result)  # Output: 8
```

### Returning Functions from Functions
```python
# Function that returns another function
def multiplier(factor):
    def multiply_by_factor(number):
        return number * factor
    return multiply_by_factor

# Using the returned function
double = multiplier(2)
print(double(5))  # Output: 10
```

### Higher-Order Functions
```python
# Using built-in higher-order functions
numbers = [1, 2, 3, 4, 5]

# Using map function
squared_numbers = map(lambda x: x**2, numbers)
print(list(squared_numbers))  # Output: [1, 4, 9, 16, 25]

# Using filter function
even_numbers = filter(lambda x: x % 2 == 0, numbers)
print(list(even_numbers))  # Output: [2, 4]
```

### Functions with Default Arguments
```python
# Function with default arguments
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

# Using the function
print(greet("Alice"))           # Output: Hello, Alice!
print(greet("Bob", "Hi"))       # Output: Hi, Bob!
```

### Functions with Variable-Length Arguments
```python
# Function with variable-length arguments (*args and **kwargs)
def example(*args, **kwargs):
    print("Positional arguments:", args)
    print("Keyword arguments:", kwargs)

# Using the function
example(1, 2, 3, key1='value1', key2='value2')
# Output:
# Positional arguments: (1, 2, 3)
# Keyword arguments: {'key1': 'value1', 'key2': 'value2'}
```

### Anonymous (Lambda) Functions
```python
# Defining and using a lambda function
multiply = lambda x, y: x * y

print(multiply(3, 4))  # Output: 12

# Using a lambda function in a higher-order function
numbers = [1, 2, 3, 4, 5]
squared_numbers = map(lambda x: x**2, numbers)
print(list(squared_numbers))  # Output: [1, 4, 9, 16, 25]
```

### Closures
```python
# Example of a closure
def outer_function(outer_var):
    def inner_function(inner_var):
        return outer_var + inner_var
    return inner_function

# Using the closure
add_five = outer_function(5)
print(add_five(10))  # Output: 15
```

### Using Functions with Decorators
```python
# Example of a decorator
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

# Calling the decorated function
say_hello()
# Output:
# Something is happening before the function is called.
# Hello!
# Something is happening after the function is called.
```

Here are examples of converting between different number types in Python:

### Converting Other Types to Boolean
```python
# Integer to boolean (non-zero is True, zero is False)
h = bool(1)
print(h)  # Output: True

i = bool(0)
print(i)  # Output: False

# Float to boolean (non-zero is True, zero is False)
j = bool(0.1)
print(j)  # Output: True

k = bool(0.0)
print(k)  # Output: False

# String to boolean (non-empty string is True, empty string is False)
l = bool("Hello")
print(l)  # Output: True

m = bool("")
print(m)  # Output: False

# List to boolean (non-empty list is True, empty list is False)
n = bool([1, 2, 3])
print(n)  # Output: True

o = bool([])
print(o)  # Output: False
```

### Converting Integers to Floats
```python
# Integer
a = 10

# Convert to float
b = float(a)
print(b)  # Output: 10.0
```

### Converting Floats to Integers
```python
# Float
c = 10.5

# Convert to integer (note: this will truncate the decimal part)
d = int(c)
print(d)  # Output: 10
```

### Converting Integers to Complex Numbers
```python
# Integer
e = 5

# Convert to complex
f = complex(e)
print(f)  # Output: (5+0j)
```

### Converting Floats to Complex Numbers
```python
# Float
g = 7.1

# Convert to complex
h = complex(g)
print(h)  # Output: (7.1+0j)
```

### Converting Strings to Integers
```python
# String
i = "123"

# Convert to integer
j = int(i)
print(j)  # Output: 123
```

### Converting Strings to Floats
```python
# String
k = "123.45"

# Convert to float
l = float(k)
print(l)  # Output: 123.45
```

These examples cover defining functions, using them as first-class objects, passing them as arguments, returning them from other functions, and using higher-order functions, default arguments, variable-length arguments, lambda functions, closures, and decorators.

In Python, the `ord` and `chr` functions are used to convert between characters and their corresponding ASCII (or Unicode) code points.

### `ord` Function
The `ord` function takes a single character as an argument and returns its corresponding ASCII (or Unicode) code point.

```python
# Using ord to get the ASCII value of a character
ascii_value = ord('A')
print(ascii_value)  # Output: 65

# Using ord with another character
ascii_value = ord('a')
print(ascii_value)  # Output: 97

# Using ord with a Unicode character
unicode_value = ord('😀')
print(unicode_value)  # Output: 128512
```

### `chr` Function
The `chr` function takes an ASCII (or Unicode) code point and returns the corresponding character.

```python
# Using chr to get the character for an ASCII value
char = chr(65)
print(char)  # Output: A

# Using chr with another ASCII value
char = chr(97)
print(char)  # Output: a

# Using chr with a Unicode code point
char = chr(128512)
print(char)  # Output: 😀
```

### Examples of Using `ord` and `chr` Together
You can use `ord` and `chr` together to encode and decode characters.

```python
# Convert a character to its ASCII value and back to a character
char = 'B'
ascii_value = ord(char)
print(ascii_value)  # Output: 66

char_back = chr(ascii_value)
print(char_back)  # Output: B
```


These examples show how to use `ord` and `chr` to work with characters and their corresponding ASCII (or Unicode) values in Python.

Certainly! Here are examples demonstrating the use of dictionaries and sets in Python, showcasing their features and common operations.

### Dictionaries

Dictionaries in Python are mutable, unordered collections of key-value pairs. They are widely used for mapping keys to values and are denoted by curly braces `{}`.

#### Example 1: Creating a Dictionary

```python
# Creating a dictionary
person = {'name': 'Alice', 'age': 30, 'city': 'Wonderland'}
print(person)  # Output: {'name': 'Alice', 'age': 30, 'city': 'Wonderland'}
```

#### Example 2: Accessing Values

```python
# Accessing values in a dictionary
print(person['name'])  # Output: Alice
print(person.get('age'))  # Output: 30
```

#### Example 3: Modifying and Adding Elements

```python
# Modifying values in a dictionary
person['age'] = 31
print(person)  # Output: {'name': 'Alice', 'age': 31, 'city': 'Wonderland'}

# Adding a new key-value pair
person['job'] = 'Engineer'
print(person)  # Output: {'name': 'Alice', 'age': 31, 'city': 'Wonderland', 'job': 'Engineer'}
```

#### Example 4: Iterating Through a Dictionary

```python
# Iterating through a dictionary
for key, value in person.items():
    print(f"{key}: {value}")

# Output:
# name: Alice
# age: 31
# city: Wonderland
# job: Engineer
```

#### Example 5: Dictionary Comprehension

```python
# Dictionary comprehension to create a new dictionary
numbers = [1, 2, 3, 4, 5]
squared_numbers = {num: num**2 for num in numbers}
print(squared_numbers)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

### Sets

Sets in Python are unordered collections of unique elements, denoted by curly braces `{}`.

#### Example 1: Creating a Set

```python
# Creating a set
fruits = {'apple', 'banana', 'orange'}
print(fruits)  # Output: {'orange', 'apple', 'banana'}
```

#### Example 2: Adding and Removing Elements

```python
# Adding elements to a set
fruits.add('pear')
print(fruits)  # Output: {'orange', 'apple', 'pear', 'banana'}

# Removing elements from a set
fruits.remove('banana')
print(fruits)  # Output: {'orange', 'apple', 'pear'}
```

#### Example 3: Set Operations

```python
# Set operations (union, intersection, difference)
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}

# Union
union_set = set1 | set2
print(union_set)  # Output: {1, 2, 3, 4, 5, 6, 7, 8}

# Intersection
intersection_set = set1 & set2
print(intersection_set)  # Output: {4, 5}

# Difference
difference_set = set1 - set2
print(difference_set)  # Output: {1, 2, 3}
```

#### Example 4: Iterating Through a Set

```python
# Iterating through a set
for fruit in fruits:
    print(fruit)

# Output:
# orange
# apple
# pear
```

#### Example 5: Set Comprehension

```python
# Set comprehension to create a new set
numbers = [1, 2, 3, 4, 5, 5, 4, 3, 2, 1]
unique_numbers = {num for num in numbers}
print(unique_numbers)  # Output: {1, 2, 3, 4, 5}
```

### Conclusion

Dictionaries and sets are versatile data structures in Python with distinct features and functionalities. Dictionaries are ideal for key-value mappings and allow efficient access and modification of data. Sets, on the other hand, are useful for storing unique elements and performing set operations such as union, intersection, and difference. Understanding these data structures and their operations will enhance your ability to work with data effectively in Python.

Exercises
---------
1. Convert "12345" into a python list [1, 2, 3, 4, 5] and vice-versa. Can you put the code inside a function?
2. Add up the ASCII values of the following strings: "Nigeria", "USA", "Africa", "Botswana", "Traveler", "misc", "madam", "@tuv".
3. Write a function to check if a number is even.
