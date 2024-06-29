Day 3: For Loops and Recursion
==============================

Morning
-------

### Reflection from Last Day:
* Answer questions about types in Python
* Discuss exercises from previous day

In Python, `for` loops are used to iterate over a sequence of items, such as elements in a list, characters in a string, or any iterable object. Here’s an introduction to `for` loops in Python, including basic syntax, examples of usage, and common patterns.

### Basic Syntax

The general syntax of a `for` loop in Python is straightforward:

```python
for item in iterable:
    # Do something with each item
    print(item)
```

- **`item`**: This variable represents the current item in the iteration. You can name it anything you like.
- **`iterable`**: This is the collection of items over which the loop iterates. It can be a list, tuple, string, range, or any iterable object.

### Example: Iterating over a List

```python
# Iterating over a list of numbers
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
# Output:
# 1
# 2
# 3
# 4
# 5
```

### Example: Iterating over a String

```python
# Iterating over a string
message = "Hello"
for char in message:
    print(char)
# Output:
# H
# e
# l
# l
# o
```

### Example: Iterating over a Range

```python
# Iterating over a range of numbers
for i in range(1, 6):  # Range from 1 to 5 (inclusive)
    print(i)
# Output:
# 1
# 2
# 3
# 4
# 5
```


### `break` and `continue` Statements

You can use `break` to exit the loop prematurely and `continue` to skip the current iteration:

```python
# Using break in a loop
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num == 3:
        break
    print(num)
# Output:
# 1
# 2

# Using continue in a loop
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num == 3:
        continue
    print(num)
# Output:
# 1
# 2
# 4
# 5
```

### Nested `for` Loops

You can nest `for` loops to iterate over multiple sequences or create patterns:

```python
# Nested for loops
for i in range(1, 4):
    for j in range(1, 4):
        print(i, j)
# Output:
# 1 1
# 1 2
# 1 3
# 2 1
# 2 2
# 2 3
# 3 1
# 3 2
# 3 3
```

### Using `enumerate` for Index and Value

You can use `enumerate` to iterate over an iterable and get both the index and value:

```python
# Using enumerate
colors = ['red', 'green', 'blue']
for index, color in enumerate(colors):
    print(index, color)
# Output:
# 0 red
# 1 green
# 2 blue
```

### Iterating Over Multiple Lists with `zip`

You can use `zip` to iterate over multiple lists simultaneously:

```python
# Using zip to iterate over multiple lists
names = ['Alice', 'Bob', 'Charlie']
ages = [25, 30, 35]
for name, age in zip(names, ages):
    print(f"{name} is {age} years old")
# Output:
# Alice is 25 years old
# Bob is 30 years old
# Charlie is 35 years old
```

### Conclusion

`for` loops are fundamental in Python for iterating over sequences and collections of data. They provide a concise way to perform repetitive tasks and are flexible enough to handle various types of data structures and iterations. Understanding these basics is crucial for effective programming in Python.


Afternoon
---------

Recursion is a programming technique where a function calls itself to solve smaller instances of the same problem. It's particularly useful for problems that can be divided into similar sub-problems. Here’s an introduction to recursion in Python, including basic concepts, examples, and key considerations.

### Basic Concepts

1. **Base Case**: The condition under which the recursive function stops calling itself. Without a base case, the function would call itself indefinitely, leading to a stack overflow.
2. **Recursive Case**: The part of the function where it calls itself with modified arguments, working towards the base case.

### Example: Factorial Function

The factorial of a non-negative integer \( n \) is the product of all positive integers less than or equal to \( n \). It's denoted as \( n! \). The factorial function can be defined recursively as follows:

- \( 0! = 1 \) (base case)
- \( n! = n \times (n-1)! \) for \( n > 0 \) (recursive case)

```python
def factorial(n):
    # Base case: factorial of 0 is 1
    if n == 0:
        return 1
    # Recursive case: n * factorial of (n-1)
    else:
        return n * factorial(n - 1)

# Testing the factorial function
print(factorial(5))  # Output: 120
```

### Example: Fibonacci Sequence

The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones. It can be defined recursively as follows:

- \( F(0) = 0 \) (base case)
- \( F(1) = 1 \) (base case)
- \( F(n) = F(n-1) + F(n-2) \) for \( n > 1 \) (recursive case)

```python
def fibonacci(n):
    # Base cases
    if n == 0:
        return 0
    elif n == 1:
        return 1
    # Recursive case
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Testing the fibonacci function
print(fibonacci(6))  # Output: 8
```

### Key Considerations

1. **Base Case**: Ensure that there is a base case to terminate the recursion. Without it, the function will recurse indefinitely and cause a stack overflow.
2. **Recursive Call**: Each recursive call should progress towards the base case to avoid infinite recursion.
3. **Performance**: Recursive solutions can be less efficient than iterative ones due to the overhead of multiple function calls. For instance, the naive recursive Fibonacci implementation has exponential time complexity. Consider using memoization or iterative solutions for performance-critical applications.

### Example: Sum of a List

Here's an example of summing the elements of a list using recursion:

```python
def sum_list(numbers):
    # Base case: empty list
    if not numbers:
        return 0
    # Recursive case: sum of the first element and the sum of the rest of the list
    else:
        return numbers[0] + sum_list(numbers[1:])

# Testing the sum_list function
print(sum_list([1, 2, 3, 4, 5]))  # Output: 15
```

### Recursion vs. Iteration

- **Recursion** is often more elegant and easier to understand for problems that have a natural recursive structure, such as tree traversals.
- **Iteration** can be more efficient in terms of memory and performance for problems that don't inherently benefit from recursion.

### Conclusion

Recursion is a powerful tool for solving problems that can be broken down into smaller, similar sub-problems. By understanding the base case and recursive case, you can effectively use recursion to solve a wide range of problems. However, always be mindful of performance implications and consider iterative solutions when appropriate.

Exercises
---------
Certainly! Here are some exercises to practice `for` loops and recursion in Python. These exercises range from basic to more advanced, covering different aspects of iteration and recursion techniques.

### Exercises for `for` Loops

1. **Sum of Numbers**: Write a function that calculates the sum of all numbers from 1 to `n` using a `for` loop.

2. **Even Numbers**: Write a function that prints all even numbers from 1 to `n` using a `for` loop.

3. **Factorial**: Write a function to compute the factorial of a number `n` using a `for` loop.

4. **Printing Patterns**: Write a program to print the following pattern using nested `for` loops:
   ```
   *
   * *
   * * *
   * * * *
   * * * * *
   ```

5. **Fibonacci Sequence**: Write a function to print the first `n` numbers in the Fibonacci sequence using a `for` loop.

6. **List Comprehension**: Convert a list of integers into their squares using list comprehension and print the result.

7. **Multiplication Table**: Write a function that prints the multiplication table (up to 10) using nested `for` loops.

8. **Prime Numbers**: Write a function to print all prime numbers up to `n` using a `for` loop and a helper function.

9. **Character Pyramid**: Write a function that prints a pyramid of characters up to a given height `n` using nested `for` loops.

### Exercises for Recursion

1. **Factorial Recursion**: Rewrite the factorial function using recursion.

2. **Fibonacci Recursion**: Write a recursive function to compute the Fibonacci sequence up to `n` numbers.

3. **Power Function**: Write a recursive function to calculate the power of a number `base` raised to an exponent `exp`.

4. **Sum of Digits**: Write a recursive function to calculate the sum of digits of a positive integer.

5. **Binary Search**: Implement the binary search algorithm recursively to find an element in a sorted list.

6. **Greatest Common Divisor (GCD)**: Write a recursive function to find the GCD of two numbers using Euclid's algorithm.

7. **Merge Sort**: Implement the merge sort algorithm using recursion to sort a list of integers.

8. **Towers of Hanoi**: Implement the Towers of Hanoi problem using recursion.

9. **Palindrome Check**: Write a recursive function to check if a given string is a palindrome.

10. **Print Paths in a Grid**: Write a recursive function to print all possible paths from the top-left corner to the bottom-right corner of a `m x n` grid.
