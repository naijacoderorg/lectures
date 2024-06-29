Day 7: Sorting Algorithms: Bubble, Selection, Insertion
=======================================================

Morning
-------

### Reflection from Last Day:
* Answer questions about searching algorithms
* Discuss exercises from previous day

Sorting algorithms are fundamental to computer science and are used to rearrange elements in a list or array into a specified order, typically numerical or lexicographical. There are numerous sorting algorithms, each with its own characteristics in terms of complexity, stability, and suitability for different data sizes and types. Here’s an introduction to some common sorting algorithms:

### 1. **Bubble Sort**
- **Description**: Bubble Sort repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.
- **Complexity**: $O(n^2)$ in the worst-case scenario.
- **Key Features**: Simple implementation, but inefficient for large data sets.

### 2. **Selection Sort**
- **Description**: Selection Sort divides the list into sorted and unsorted parts. It repeatedly selects the smallest (or largest) element from the unsorted part and swaps it with the first unsorted element.
- **Complexity**: $O(n^2)$ in all cases.
- **Key Features**: Simple implementation, but also inefficient for large data sets.

### 3. **Insertion Sort**
- **Description**: Insertion Sort builds the final sorted array one item at a time. It takes each element from the list and inserts it into its correct position relative to the sorted portion of the array.
- **Complexity**: $O(n^2)$ in the worst-case scenario, but $O(n)$ when the list is nearly sorted.
- **Key Features**: Efficient for small data sets or when the input array is almost sorted.

### 4. **Merge Sort**
- **Description**: Merge Sort is a divide-and-conquer algorithm. It divides the input array into two halves, recursively sorts each half, and then merges the sorted halves to produce the final sorted array.
- **Complexity**: $O(n \log n)$ in all cases.
- **Key Features**: Stable sort (keeps the order of equal elements), efficient for large data sets, but requires additional memory proportional to the size of the input.

### 5. **Quick Sort**
- **Description**: Quick Sort is another divide-and-conquer algorithm. It picks an element as a pivot and partitions the array around the pivot, such that elements less than the pivot are on the left and elements greater than the pivot are on the right. It then recursively sorts the sub-arrays.
- **Complexity**: $O(n \log n)$ in the average case, $O(n^2)$ in the worst-case scenario (rare).
- **Key Features**: Efficient for large data sets, in-place (requires only a small additional memory), and often faster than Merge Sort in practice.


### Choosing the Right Algorithm

- **Efficiency**: Consider the size of the data set and the expected range of data values.
- **Stability**: Whether the algorithm maintains the relative order of equal elements.
- **Memory Usage**: Some algorithms require additional memory for operations.
- **Application**: Different algorithms may be more suitable depending on the specific requirements and characteristics of the data.

Each sorting algorithm has its trade-offs in terms of time complexity, space complexity, and practical performance characteristics. The choice of sorting algorithm depends on the specific requirements of the application, such as input size, data characteristics, stability, and performance constraints.

Insertion Sort is a simple sorting algorithm that builds the final sorted array (or list) one element at a time. It is efficient for small data sets or when the input array is almost sorted. Here's an introduction to Insertion Sort:

### Description

Insertion Sort works similarly to how you might sort playing cards in your hands. You start with an empty left hand and the cards face down on the table. You then remove one card at a time from the table and insert it into the correct position in your left hand, maintaining the cards in your left hand sorted.

### Steps

1. **Initialization**: Start with the second element (index 1) and consider it as part of the sorted portion.

2. **Comparison and Insertion**: For each element, compare it with the elements in the sorted portion (left side). Shift all the elements greater than the current element to the right. Insert the current element into its correct position.

3. **Repeat**: Repeat the process until the entire array is sorted.

### Example

Let's sort the array `[5, 2, 4, 6, 1, 3]` using Insertion Sort:

- **Initial Array**: `[5, 2, 4, 6, 1, 3]`

1. Start with the second element (`2`):
   - Compare `2` with `5` (first element). Since `2 < 5`, swap them.
   - Array becomes `[2, 5, 4, 6, 1, 3]`.

2. Consider the third element (`4`):
   - Compare `4` with `5` (previous element). Since `4 < 5`, swap them.
   - Array becomes `[2, 4, 5, 6, 1, 3]`.
   - Compare `4` with `2` (previous element). No swap needed.

3. Continue with each subsequent element, shifting larger elements as necessary and inserting the current element into its correct position.

4. After sorting, the array becomes `[1, 2, 3, 4, 5, 6]`.

### Complexity

- **Time Complexity**: $O(n^2)$ in the worst-case scenario (when the array is reverse sorted), and $O(n)$ in the best-case scenario (when the array is already sorted).
- **Space Complexity**: $O(1)$ additional space, as it sorts in-place.

### Implementation (Python)

Here's a simple implementation of Insertion Sort in Python:

```python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        current_value = arr[i]
        j = i - 1
        while j >= 0 and arr[j] > current_value:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = current_value

# Example usage:
arr = [5, 2, 4, 6, 1, 3]
insertion_sort(arr)
print("Sorted array:", arr)
```

In this implementation:
- We iterate over each element in the array starting from index 1.
- For each element, we compare it with the elements to its left in the sorted portion of the array and insert it into its correct position by shifting larger elements to the right.

Insertion Sort is intuitive and straightforward to implement, making it suitable for small data sets or scenarios where the input is mostly sorted. However, for large data sets, more efficient algorithms like Merge Sort or Quick Sort are generally preferred due to their better average-case performance.

Selection Sort is a simple and intuitive sorting algorithm that divides the input list into a sorted and an unsorted region. It repeatedly selects the smallest (or largest, depending on the sorting order) element from the unsorted region and swaps it with the first element of the unsorted region. Here’s an introduction to Selection Sort:

### Description

Selection Sort works by finding the minimum element from the unsorted portion of the list and swapping it with the first unsorted element. It continues this process, gradually reducing the unsorted region until the entire list is sorted.

### Steps

1. **Initialization**: Start with the entire list considered as unsorted.

2. **Finding the Minimum**: Iterate through the unsorted region to find the minimum element.

3. **Swapping**: Swap the minimum element with the first element of the unsorted region.

4. **Repeat**: Continue the process for the remaining unsorted region until the list is sorted.

### Example

Let's sort the array `[64, 25, 12, 22, 11]` using Selection Sort:

- **Initial Array**: `[64, 25, 12, 22, 11]`

1. **First Pass**: Find the smallest element and swap it with the first element:
   - `[11, 25, 12, 22, 64]` (swap `11` with `64`)

2. **Second Pass**: Consider the remaining unsorted region (`[25, 12, 22, 64]`):
   - `[11, 12, 25, 22, 64]` (swap `12` with `25`)

3. **Third Pass**: Continue with the remaining unsorted region (`[25, 22, 64]`):
   - `[11, 12, 22, 25, 64]` (swap `22` with `25`)

4. **Fourth Pass**: Continue with the remaining unsorted region (`[64]`):
   - `[11, 12, 22, 25, 64]` (no swap needed)

5. **Final Sorted Array**: `[11, 12, 22, 25, 64]`

### Complexity

- **Time Complexity**: $O(n^2)$ in all cases (worst-case, average-case, and best-case scenarios).
- **Space Complexity**: $O(1)$ additional space, as it sorts in-place.

### Implementation (Python)

Here's a simple implementation of Selection Sort in Python:

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        # Find the minimum element in remaining unsorted array
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        
        # Swap the found minimum element with the first element of unsorted array
        arr[i], arr[min_index] = arr[min_index], arr[i]

# Example usage:
arr = [64, 25, 12, 22, 11]
selection_sort(arr)
print("Sorted array:", arr)
```

In this implementation:
- We iterate through the list and find the index of the smallest element in the unsorted region.
- We swap this smallest element with the first element of the unsorted region.
- We repeat this process until the entire array is sorted.

Selection Sort is straightforward to implement and understand, making it suitable for educational purposes or situations where simplicity is preferred. However, it is less efficient compared to more advanced sorting algorithms like Merge Sort or Quick Sort, especially for larger data sets.

Afternoon
---------

Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. It passes through the list multiple times until the list is sorted. Here's an introduction to Bubble Sort:

### Description

Bubble Sort gets its name because smaller or larger elements "bubble" to the top (beginning) of the list in each pass. It works by repeatedly comparing adjacent elements and swapping them if they are in the wrong order. After each pass, the largest (or smallest, depending on the sorting order) element is guaranteed to be in its correct position. This process is repeated for each element in the list.

### Steps

1. **Passes through the List**: Start with the first element and compare it with the next element. If they are in the wrong order, swap them.

2. **Repeated Passes**: Continue making passes through the list until no more swaps are needed, which indicates that the list is sorted.

3. **Complexity**: The algorithm's efficiency improves as larger elements (or smaller ones) are sorted and "bubble up" towards their correct positions.

### Example

Let's sort the array `[5, 2, 4, 6, 1, 3]` using Bubble Sort:

- **Initial Array**: `[5, 2, 4, 6, 1, 3]`

1. **First Pass**: Compare adjacent elements and swap if necessary:
   - `[2, 5, 4, 6, 1, 3]` (swap `5` and `2`)
   - `[2, 4, 5, 6, 1, 3]` (swap `5` and `4`)
   - `[2, 4, 5, 6, 1, 3]` (no swap needed)
   - `[2, 4, 5, 1, 6, 3]` (swap `6` and `1`)
   - `[2, 4, 5, 1, 3, 6]` (swap `6` and `3`)

2. **Second Pass**: Continue with the remaining unsorted elements:
   - `[2, 4, 1, 5, 3, 6]`
   - `[2, 4, 1, 3, 5, 6]`
   - `[2, 1, 4, 3, 5, 6]`
   - `[2, 1, 3, 4, 5, 6]`

3. **Final Pass**: The array is now sorted:
   - `[1, 2, 3, 4, 5, 6]`

### Complexity

- **Time Complexity**: $O(n^2)$ in the worst-case scenario (when the array is reverse sorted) and in the average-case scenario. $O(n)$ in the best-case scenario (when the array is already sorted).
- **Space Complexity**: $O(1)$ additional space, as it sorts in-place.

### Implementation (Python)

Here's a simple implementation of Bubble Sort in Python:

```python
def bubble_sort(arr):
    n = len(arr)
    # Traverse through all array elements
    for i in range(n):
        # Last i elements are already in place, so no need to check them
        for j in range(0, n-i-1):
            # Swap if the element found is greater than the next element
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

# Example usage:
arr = [5, 2, 4, 6, 1, 3]
bubble_sort(arr)
print("Sorted array:", arr)
```

In this implementation:
- We iterate over the array multiple times.
- For each pass, we compare adjacent elements and swap them if they are in the wrong order.
- The algorithm terminates early if no swaps are needed during a pass, indicating that the list is already sorted.

Bubble Sort is straightforward to implement and understand but is generally inefficient for large data sets compared to more advanced sorting algorithms like Merge Sort or Quick Sort.

Exercises
---------

### Insertion Sort Exercises

1. **Exercise 1: Implement Insertion Sort**
   - **Problem**: Write a function `insertion_sort(arr)` that sorts an array `arr` using Insertion Sort.

2. **Exercise 2: Count Inversions**
   - **Problem**: Modify the `insertion_sort` function to count the number of inversions in the array. An inversion is a pair of elements `(arr[i], arr[j])` such that `i < j` and `arr[i] > arr[j]`.

3. **Exercise 3: Sort Characters in a String**
   - **Problem**: Write a function `sort_string(s)` that sorts the characters in a string `s` using Insertion Sort and returns the sorted string.

### Bubble Sort Exercises

1. **Exercise 4: Implement Bubble Sort**
   - **Problem**: Write a function `bubble_sort(arr)` that sorts an array `arr` using Bubble Sort.

2. **Exercise 5: Optimized Bubble Sort**
   - **Problem**: Modify the `bubble_sort` function to implement an optimized version of Bubble Sort that terminates early if no swaps are made in a pass.

3. **Exercise 6: Bubble Sort for Linked List**
   - **Problem**: Implement Bubble Sort to sort a singly linked list.
