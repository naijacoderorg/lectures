Day 5: Objects, Libraries, Data Science
=======================================

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

Afternoon - Data Science Part 1
---------

### Applied Data Science: Tackling Climate Change

Lecture from Alida on applying data analytics and computer science to tackling climate change. 

### What is a Python Library?

A Python library is a collection of functions and methods that allows you to perform specific tasks without having to write the code yourself from scratch. Libraries are designed to be reusable, saving development time and effort by providing pre-written solutions to common programming challenges.

### Popular Python Libraries

Python has a vast ecosystem of libraries covering various domains. Some popular libraries include:

- **Pandas**: Data analysis library that provides high-performance data structures and tools for manipulating structured data.
- **NumPy**: Numerical computing library for handling large arrays and matrices of numeric data.
- **Matplotlib**: 2D plotting library for creating static, animated, and interactive visualizations.
- **Requests**: HTTP library for making HTTP requests and interacting with web APIs.
- **Django**: Web framework for building web applications using the model-template-views (MTV) architectural pattern.
- **Flask**: Lightweight web framework for building web applications with a flexible and modular structure.
- **TensorFlow** and **PyTorch**: Libraries for machine learning and deep learning, providing tools for building and training neural networks.
- **NLTK (Natural Language Toolkit)**: Library for natural language processing (NLP) tasks such as tokenization, stemming, tagging, parsing, and more.

**We will mainly use `pandas` for our data science work, so let us learn how to install and import it into Python.**

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

### Introduction to Data Science

Data science is a growing field that combines mathematics, statistics, and computer science to extract meaningful insights from data. By analyzing and interpreting large amounts of information, data scientists can uncover patterns, make predictions, and help solve complex problems. In this introduction to data science, you will learn how to use Python to analyze real-world data.

### Japa!

Every data science project begins with data, and understanding the context behind the data is crucial for gaining meaningful insights.

Our dataset is extracted from the [World Bank's](https://databank.worldbank.org/source/global-bilateral-migration) Global Bilateral Migration database. The dataset provides detailed information on international migration patterns between countries. It includes data on the number of migrants by origin and destination countries, from 1960 to 2000, in ten-year intervals. This dataset can help in analyzing migration trends, demographic changes, and the impacts of migration on economies and societies globally. It is a valuable resource for researchers, policymakers, and organizations involved in migration studies and related fields.

**For our project, we will use a subset of this data containing only migrations flows that originate from an African origin country.**

Let's spend some time exploring the dataset.

### Load the data

We begin by loading the data into Python using the `pandas` library which offers many useful functions for reading data. Our dataset is a CSV file stored in a GitHub repository; hence, we will use its URL with the `read_csv()` function to access it. _You can find more examples on reading in csv files [here](https://www.geeksforgeeks.org/reading-csv-files-in-python/)._

```python
import pandas as pd

url = 'https://raw.githubusercontent.com/naijacoderorg/lectures/main/lectures2024/day5/migration_africa.csv'
df = pd.read_csv(url)
```
df is short form for DataFrame. It's a lazy way to name our initial dataset. We should be more specific in our naming in the future.

### Pandas DataFrame Attributes and Methods

Let's check what class our data object has inherited.

```python
df.__class__ # check for the class of df
```
As a pandas dataframe, our `df` object has certain attributes and methods. An attribute in programming is a property of an object that stores data about that object. A method is a function that can perform an action on an object of the specified class. Both attributes and methods are accessed using dot notation, but methods additionally have parentheses `()` because they are functions, even when no arguments are specified.

Let's explore some DataFrame attributes and methods for our dataset.

#### `.head()` displays the first few rows of the DataFrame

By default, only the first five rows are displayed. To get a different number of rows, you can specify that in the argument, like `df.head(10)`.

```python
df.head()
```

Our dataset is tabular. This means that it has rows and columns. The rows represent a single observation, and the columns are features that contain specific information (like country of origin) on each observation. 

Whenever we explore a dataset, one of the first questions we should ask ourselves is this: **What is the level of an observation?** Can you describe what information a specific row gives you?

In this case, each row of the dataset represents a specific migration flow over time. For example, the first row shows the number of migrations from Nigeria (the origin) to Afghanistan (the destination) for the years 1960, 1970, 1980, 1990, and 2000. We always spend time ensuring that we understand what each observation represents as the rest of our analysis is hinged on this knowledge.

#### `.shape` displays the number of rows and columns

We can also check for the dimensions (number of rows and columns) of our dataset using the `.shape` attribute. Try to interpret the result you get? Why do you think the dataset is this large? We'll explore this later, but feel free to brainstorm now.

```python
df.shape
```

Try out the following attributes and methods to learn more about your dataset.
+ df.columns
+ df.dtypes
+ df.index
+ df.size
+ df.values
+ df.info()
+ df.describe()
+ df.isnull().sum()

### Asking Good Data Questions

In our next Data Science session, we will spend some time exploring the data more deeply and finding exact answers to questions we have about the data. But today, we need to learn how to generate effective data questions that can lead to valuable insights and informed decision-making.

### Principles for Formulating Good Data Questions

#### 1. Specificity

- Good questions are specific. Vague questions lead to unclear answers. Specific questions narrow down the focus and make it easier to find precise answers.
- Example: Instead of asking "How are our sales?", ask "How did our sales perform in the last quarter compared to the previous quarter?"

#### 2. Measurability

- Questions should be measurable and quantifiable. If you can't measure it, you can't analyze it.
- Example: "What is the average customer satisfaction score for the past six months?" rather than "Are our customers happy?"

#### 3. Relevance:

- Questions should be relevant to the business goals or research objectives. They should address a real need or problem.
- Example: "Which marketing channel has the highest return on investment in the past year?" is more relevant than "What are all the marketing channels we use?"

#### 4. Actionability:

- A good data question leads to actionable insights. The answers should help make decisions or drive actions.
- Example: "What are the top three reasons customers are canceling their subscriptions?" This can lead to actions to reduce churn.

In our work this week, we will ensure that our questions always satisfy Principles 1 and 2. While our questions may not always meet Principles 3 and 4, these principles will become more useful as we begin practicing asking data questions in real-world situations beyond this camp.

### Steps to Formulate Good Data Questions:

#### 1. Identify the Objective:

- Start by understanding the problem or goal. What do you want to achieve with this analysis?
- Example: If the goal is to increase sales, your questions should focus on factors influencing sales.

#### 2. Break Down the Problem:

- Divide the main objective into smaller, more manageable questions.
- Example: Instead of "How can we increase sales?", ask "Which products have seen a decline in sales?", "Which customer segments are underperforming?", and "Which marketing campaigns were most effective?"

#### 3. Consider the Data Available:

- Ensure that the questions can be answered with the data you have or can realistically obtain.
- Example: If you have sales data by region, you can ask "Which regions have the highest growth in sales?"

#### 4. Iterate and Refine:

- Continuously refine your questions based on initial findings and feedback.
- Example: After analyzing the initial sales data, you might refine the question to focus on a specific product line or customer segment.

### Brainstorming Activity

In small groups, let's practice coming up with good questions based on our dataset. In your group, brainstorm a list of specific, measurable, (relevant), and (actionable) questions that you would ask.

When the time is up, you will present your questions to the class.


Exercises
---------

### Homework for Next Week
1. Read chapter 1 (The Role of Algorithms in Computing) in CLRS
2. Read chapter 2 (Getting Started) in CLRS
3. Read chapter 3 (Growth of Functions) in CLRS