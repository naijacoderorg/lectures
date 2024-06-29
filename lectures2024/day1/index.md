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
