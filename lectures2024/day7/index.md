Day 7: Searching Algorithms
===========================

Morning
-------

### Reflection from Last Day:
* Answer questions about for asymptotic notation and growth of functions
* Discuss exercises from previous day

Searching algorithms are fundamental methods used to locate elements within a data structure, such as arrays, lists, trees, graphs, and more. In Python, these algorithms are crucial for efficiently finding specific items based on certain criteria. Here’s an introduction to some commonly used searching algorithms:

### Linear Search

**Linear search** is the simplest form of searching algorithm where each element in the list is checked sequentially until the target element is found or the end of the list is reached.

- **Time Complexity**: $O(n)$ - Linear time complexity, where n is the number of elements in the list.

#### Example of Linear Search in Python:

```python
def linear_search(arr, target):
    for i in range(len(arr)):
        if arr[i] == target:
            return i  # Return index if found
    return -1  # Return -1 if not found

# Example usage
my_list = [10, 30, 20, 5, 15]
target_value = 20
result = linear_search(my_list, target_value)
if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")
```


Afternoon
---------


### Binary Search

**Binary search** is a more efficient searching algorithm that requires the list to be sorted. It works by repeatedly dividing the search interval in half. If the target value matches the middle element, its position is returned. Otherwise, the search continues in either the left or right half, depending on whether the target value is less than or greater than the middle element.

- **Time Complexity**: $O(\log n)$ - Logarithmic time complexity, where n is the number of elements in the sorted list.

#### Example of Binary Search in Python:

```python
def binary_search(arr, target):
    low = 0
    high = len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid  # Return index if found
        elif arr[mid] < target:
            low = mid + 1  # Search in the right half
        else:
            high = mid - 1  # Search in the left half
    return -1  # Return -1 if not found

# Example usage
sorted_list = [5, 10, 15, 20, 30]
target_value = 20
result = binary_search(sorted_list, target_value)
if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")
```

### Key Considerations

- **Data Structure**: The choice of searching algorithm often depends on the data structure being used (e.g., lists, trees, graphs).
- **Performance**: Binary search is significantly faster than linear search for large datasets, especially when the data is sorted.
- **Edge Cases**: Consider edge cases such as empty lists or arrays with duplicate values when implementing and testing searching algorithms.

Exercises
---------

### Linear Search Exercises

1. **Exercise 1: Finding an Element**
   - **Problem**: Implement a function `linear_search(arr, target)` that returns the index of `target` in the list `arr` using linear search. If `target` is not present, return `-1`.
   - **Example**:
     ```python
     arr = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
     target = 5
     # Output: 4 (index of the first occurrence of 5)
     ```
     Use a while loop!

2. **Exercise 2: Counting Occurrences**
   - **Problem**: Modify the previous function to return the number of times `target` appears in `arr`.
   - **Example**:
     ```python
     arr = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
     target = 5
     # Output: 2 (number of times 5 appears in arr)
     ```

3. **Exercise 3: Sum of Elements**
   - **Problem**: Write a function `sum_linear_search(arr)` that computes the sum of all elements in the list `arr` using linear search.
   - **Example**:
     ```python
     arr = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
     # Output: 39 (sum of all elements in arr)
     ```

### Binary Search Exercises

1. **Exercise 4: Basic Binary Search**
   - **Problem**: Implement a function `binary_search(arr, target)` that performs binary search on a sorted list `arr` to find the index of `target`. If `target` is not present, return `-1`.
   - **Example**:
     ```python
     arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
     target = 6
     # Output: 5 (index of 6 in arr)
     ```
Use a for loop or recursion!

2. **Exercise 5: Finding Smallest Element**
   - **Problem**: Modify the binary search function to find the smallest element in a rotated sorted array `rotated_arr`.
   - **Example**:
     ```python
     rotated_arr = [4, 5, 6, 7, 0, 1, 2]
     # Output: 0 (smallest element in rotated_arr)
     ```

3. **Exercise 6: Counting Elements**
   - **Problem**: Write a function `count_binary_search(arr, target)` that counts the number of occurrences of `target` in a sorted list `arr` using binary search.
   - **Example**:
     ```python
     arr = [1, 2, 2, 2, 3, 4, 5, 5, 6]
     target = 2
     # Output: 3 (number of times 2 appears in arr)
     ```
