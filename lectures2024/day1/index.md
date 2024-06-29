Day 1: Introductions and Motivations
=====================================

Morning
-------

**Introductions**: 
* Instructors introduce themselves; students introduce themselves.
* Discussion on computer science, data science, and mathematics networks in Nigeria.
* Make sure they can log in to computers and have a google account for Google Colab.
* Emphasize the goal: for them to become scientists, engineers, and mathematicians.

**Keynote**: Jelani Nelson (1-2 hours for discussion with students, instructors)

**Main Textbook**: Share CLRS textbook with students; take cursory look at the topics to cover [1].

[1] “Introduction to Algorithms” 
By Thomas H. Cormen, Charles E. Leiserson, Ronald L. Rivest, and Clifford Stein.


Afternoon
---------

Start reading chapter 1 of CLRS. 
In-class exercises:
1.1-1 up to 1.1-5. 1.2-1 up to 1.2-3. And 1-1 (implement using python time module).
1-1.
Leave the rest as homework.

In Python, variables are used to store data values. Unlike some other programming languages, Python does not require explicitly declaring the data type of a variable when it is created. Instead, Python uses dynamic typing, where variables can dynamically change their type based on the value assigned to them.

### Variable Naming Rules

When naming variables in Python, you need to follow these rules:

- Variable names must start with a letter (a-z, A-Z) or an underscore (`_`). They cannot start with a number.
- Variable names can only contain letters, numbers, and underscores (`_`).
- Variable names are case-sensitive (`age`, `Age`, and `AGE` are three different variables).
- Python keywords (like `if`, `else`, `for`, etc.) cannot be used as variable names.

### Variable Assignment

Variables in Python are assigned using the assignment operator `=`. You can assign a value to a variable using this syntax:

```python
variable_name = value
```

#### Example 1: Assigning Values to Variables

```python
# Assigning values to variables
name = "Alice"
age = 30
is_student = False
```

### Variable Types

Python supports various types of variables, including:

- **Integers (`int`)**: Whole numbers without a decimal point.
- **Floating-point numbers (`float`)**: Numbers that have a decimal point or use exponential (e.g., `1.23`, `3.45e-6`).
- **Strings (`str`)**: Textual data enclosed within quotes (`'single'` or `"double"`).
- **Booleans (`bool`)**: Represents truth values (`True` or `False`).
- **Lists (`list`)**: Ordered collections of items, mutable.
- **Tuples (`tuple`)**: Ordered collections of items, immutable.
- **Dictionaries (`dict`)**: Unordered collections of key-value pairs.

### Example 2: Variables of Different Types

```python
# Variables of different types
age = 30              # Integer
average_grade = 85.5  # Float
student_name = "Bob"  # String
is_passing = True     # Boolean
```

### Variable Reassignment

Variables in Python can be reassigned to different values of any type. This is due to Python's dynamic typing nature.

#### Example 3: Reassigning Variables

```python
# Reassigning variables
age = 30
print(age)  # Output: 30

age = "thirty"
print(age)  # Output: thirty
```

### Printing Variables

You can display the value of a variable using the `print()` function.

#### Example 4: Printing Variables

```python
# Printing variables
name = "Alice"
print("Hello,", name)  # Output: Hello, Alice
```

### Conclusion

Variables in Python are essential for storing and manipulating data in your programs. They are dynamically typed and flexible, allowing you to work with different types of data seamlessly. Understanding how to declare, assign, and use variables effectively is fundamental to writing Python code.

In Python, comments are used to annotate code for various purposes such as explaining functionality, providing documentation, or temporarily disabling code. Comments are ignored by the Python interpreter during execution and are purely for human readers. They help improve code readability and understanding, especially for yourself and other developers who may work on the code later.

### Types of Comments in Python

Python supports two types of comments:

#### 1. Single-line Comments

Single-line comments begin with the `#` character and continue until the end of the line. They are typically used for short comments on a single line of code.

##### Example of Single-line Comment:

```python
# This is a single-line comment
x = 5  # Assigning value 5 to variable x
```

#### 2. Multi-line Comments (Docstrings)

Multi-line comments, also known as docstrings, are used for documenting modules, classes, functions, or methods. They are enclosed in triple quotes (`""" """` or `''' '''`) and can span multiple lines. While docstrings are primarily used for documentation, they can also be used as multi-line comments.

##### Example of Multi-line Comment (Docstring):

```python
"""
This is a multi-line comment (docstring).
It can span multiple lines and is used for documentation.
"""
```

### Best Practices for Using Comments

- **Use Comments Sparingly**: Write code that is self-explanatory where possible. Use comments to clarify complex logic or important details.
- **Be Clear and Concise**: Write clear comments that explain the intent or purpose of the code without stating the obvious.
- **Update Comments**: Keep comments up-to-date with the code. If you modify the code's behavior, ensure the corresponding comments are also updated.
- **Avoid Redundant Comments**: Avoid comments that simply repeat what the code is doing. Comments should provide additional context or explain why something is done a certain way.
- **Use Docstrings for Documentation**: Use docstrings to document classes, functions, and methods according to Python's documentation conventions (PEP 257).

### Example of Good Commenting Practices

```python
# Calculate the area of a rectangle
length = 5
width = 3
area = length * width  # Formula: length * width
print(f"The area of the rectangle is {area}")
```

### When to Use Comments

- **Explanation of Code**: Explain complex algorithms or logic that might not be immediately clear.
- **TODO Comments**: Mark places where you intend to add more code or improvements in the future (`# TODO: Implement error handling`).
- **Debugging**: Temporarily comment out code for debugging purposes (`# print(some_variable)`).
- **Documentation**: Use docstrings to document modules, classes, functions, and methods for generating documentation using tools like Sphinx.

### Conclusion

Comments in Python are valuable for enhancing code readability, explaining functionality, and providing documentation. By using comments effectively and following best practices, you can create code that is easier to understand, maintain, and collaborate on with other developers.
