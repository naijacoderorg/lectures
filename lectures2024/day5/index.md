Day 5: Objects, Libraries
=========================

Morning
-------

### Reflection from Last Day:
* Answer questions about for iteration in Python
* Discuss exercises from previous day

In Python, objects and classes are fundamental concepts used in object-oriented programming (OOP). Object-oriented programming is a programming paradigm that focuses on creating objects that encapsulate data and behavior together. Here's an introduction to objects, classes, and how they are used in Python:

### Objects

An object is an instance of a class. It encapsulates data (attributes) and behaviors (methods). In Python, almost everything is an object, including integers, floats, strings, lists, and more complex structures like functions and classes themselves.

#### Example of Objects:

```python
# Examples of objects
x = 5         # Integer object
name = "Alice"  # String object
my_list = [1, 2, 3]  # List object
```

### Classes

A class is a blueprint for creating objects (instances). It defines a set of attributes and methods that characterize any object of the class. Think of a class as a template or a blueprint that describes the attributes and behaviors common to all objects of that class.

#### Defining a Class:

In Python, a class is defined using the `class` keyword followed by the class name and a colon `:`. Inside the class definition, you define attributes and methods.

##### Example of Class Definition:

```python
# Class definition
class Person:
    # Constructor (initializing attributes)
    def __init__(self, name, age):
        self.name = name   # Attribute: name
        self.age = age     # Attribute: age
    
    # Method to greet
    def greet(self):
        return f"Hello, my name is {self.name} and I am {self.age} years old."

# Creating objects (instances) of the Person class
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

# Using object methods
print(person1.greet())  # Output: Hello, my name is Alice and I am 30 years old.
print(person2.greet())  # Output: Hello, my name is Bob and I am 25 years old.
```

#### Anatomy of a Class:

- **Attributes**: Variables that store data (state) related to the object (`self.name`, `self.age`).
- **Methods**: Functions defined inside a class that can perform operations on the object (`greet()`).

#### Constructor (`__init__` method):

The `__init__` method is a special method in Python classes that is called when an object is instantiated. It initializes the object's attributes. The first parameter of `__init__` and all instance methods is `self`, which refers to the instance of the class itself.

### Key Concepts in OOP

- **Encapsulation**: Bundling data (attributes) and methods (functions) that operate on the data into a single unit (object).
- **Inheritance**: Creating new classes (derived classes or subclasses) from existing classes (base classes or superclasses) to reuse and extend functionality.
- **Polymorphism**: The ability to use a single interface (method) to perform different tasks. In Python, polymorphism is achieved through method overriding and method overloading.

### Benefits of OOP

- **Modularity**: Encapsulation allows for easier maintenance and modification of code.
- **Reusability**: Classes and objects promote code reuse through inheritance.
- **Flexibility and Scalability**: OOP makes it easier to manage and scale complex applications by organizing code into manageable pieces.

### Conclusion

Understanding objects and classes in Python is crucial for leveraging the power of object-oriented programming. By defining classes and creating objects, you can organize your code more effectively, promote code reuse, and build complex, scalable applications more efficiently. OOP is a powerful paradigm that enhances code organization, readability, and maintainability in Python and many other programming languages.

Afternoon
---------

Using Python libraries is fundamental for leveraging pre-written code that provides functionalities beyond the core Python language. Libraries are collections of modules and functions that extend Python's capabilities, enabling you to perform specialized tasks such as data analysis, web development, machine learning, and more. Here's an introduction to using Python libraries effectively:

### What is a Python Library?

A Python library is a collection of functions and methods that allows you to perform specific tasks without having to write the code yourself from scratch. Libraries are designed to be reusable, saving development time and effort by providing pre-written solutions to common programming challenges.

### Popular Python Libraries

Python has a vast ecosystem of libraries covering various domains. Some popular libraries include:

- **NumPy**: Numerical computing library for handling large arrays and matrices of numeric data.
- **Pandas**: Data analysis library that provides high-performance data structures and tools for manipulating structured data.
- **Matplotlib**: 2D plotting library for creating static, animated, and interactive visualizations.
- **Requests**: HTTP library for making HTTP requests and interacting with web APIs.
- **Django**: Web framework for building web applications using the model-template-views (MTV) architectural pattern.
- **Flask**: Lightweight web framework for building web applications with a flexible and modular structure.
- **TensorFlow** and **PyTorch**: Libraries for machine learning and deep learning, providing tools for building and training neural networks.
- **NLTK (Natural Language Toolkit)**: Library for natural language processing (NLP) tasks such as tokenization, stemming, tagging, parsing, and more.

### Using Python Libraries

#### 1. Installing Libraries

Before using a library, you need to install it. Python's package manager `pip` is used for installing libraries from the Python Package Index (PyPI).

```bash
pip install library_name
```

Replace `library_name` with the name of the library you want to install (e.g., `numpy`, `pandas`, `matplotlib`).

#### 2. Importing Libraries

Once installed, you import the library into your Python script or interactive session using the `import` statement. You can also use `import ... as ...` to create an alias for the library name.

##### Example: Importing NumPy and Pandas

```python
import numpy as np
import pandas as pd
```

#### 3. Using Library Functions and Classes

After importing the library, you can use its functions, classes, and constants in your code. Refer to the library's documentation for details on available functionalities and usage examples.

##### Example: Using NumPy and Pandas

```python
# Using NumPy for array operations
arr = np.array([1, 2, 3, 4, 5])
print("Sum:", np.sum(arr))  # Output: Sum: 15

# Using Pandas for data manipulation
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'Age': [25, 30, 35]}
df = pd.DataFrame(data)
print(df)
```

#### 4. Exploring Documentation and Examples

Each library has comprehensive documentation that includes installation instructions, usage guides, and examples. Refer to the official documentation or community resources (like Stack Overflow) for help and examples specific to your use case.

### Conclusion

Python libraries expand the capabilities of Python beyond its core features, allowing you to efficiently tackle a wide range of tasks and domains. By leveraging libraries, you can accelerate development, improve code quality, and access powerful tools and algorithms developed and maintained by the Python community and experts worldwide. Familiarize yourself with the libraries relevant to your projects to maximize productivity and effectiveness in Python programming.

Exercises
---------

### Exercise 1: Using NumPy

1. **Create a NumPy array**: Create a 1D array of integers from 1 to 10.
2. **Calculate statistics**: Compute the mean, median, and standard deviation of the array.
3. **Reshape the array**: Reshape the array into a 2D matrix with 2 rows and 5 columns.
4. **Perform element-wise operations**: Multiply each element of the matrix by 2.
5. **Indexing and slicing**: Extract the second row of the matrix.

### Exercise 2: Using Pandas

1. **Create a DataFrame**: Create a Pandas DataFrame from a dictionary with columns 'Name', 'Age', and 'City'.
2. **Read from CSV**: Load a CSV file into a DataFrame using `pd.read_csv()`.
3. **Data manipulation**: Add a new column 'Salary' to the DataFrame with random salary values.
4. **Filtering and querying**: Filter rows where 'Age' is greater than 30 and 'City' is 'New York'.
5. **Grouping and aggregation**: Group the data by 'City' and calculate the average salary for each city.

### Exercise 3: Using Matplotlib

1. **Line plot**: Plot a simple line graph of `y = sin(x)` for values of `x` from 0 to 2π.
2. **Scatter plot**: Generate random data points (x, y) and plot them as a scatter plot.
3. **Histogram**: Create a histogram of random data with 50 bins.
4. **Customizing plots**: Customize the plot by adding labels to axes, a title, and a legend (if applicable).
5. **Subplots**: Create a figure with multiple subplots, each displaying different types of plots (e.g., line plot, scatter plot).

### Exercise 4: Combined Exercises

1. **Data manipulation and visualization**: Load a dataset (e.g., from Seaborn's built-in datasets or CSV), perform data manipulation using Pandas (e.g., filtering, grouping), and visualize the results using Matplotlib (e.g., bar plot, box plot).

### Example Solutions

Here's a brief example of how you might approach Exercise 1 using NumPy:

```python
import numpy as np

# Exercise 1: Using NumPy
# 1. Create a NumPy array
array = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

# 2. Calculate statistics
mean = np.mean(array)
median = np.median(array)
std_dev = np.std(array)

print(f"Mean: {mean}, Median: {median}, Standard Deviation: {std_dev}")

# 3. Reshape the array
matrix = array.reshape(2, 5)
print("Reshaped matrix:\n", matrix)

# 4. Perform element-wise operations
matrix *= 2
print("Matrix after multiplying by 2:\n", matrix)

# 5. Indexing and slicing
second_row = matrix[1, :]
print("Second row of matrix:", second_row)
```
