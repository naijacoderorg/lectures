Day 9: Sorting Algorithms: Part 2
=================================


### Reflection from Last Day:
* Answer questions about sorting algorithms
* Discuss exercises from previous day

Quicksort is a highly efficient sorting algorithm and is based on the divide-and-conquer strategy. It works by selecting a 'pivot' element from the array and partitioning the other elements into two sub-arrays according to whether they are less than or greater than the pivot. The sub-arrays are then recursively sorted.

### Description

Quicksort follows these steps:

1. **Choose a Pivot**: Select an element from the array as the pivot. There are various ways to choose a pivot, such as picking the first element, the last element, a random element, or using a median-of-three approach.

2. **Partitioning**: Rearrange the array so that all elements less than the pivot are on the left side of the pivot, and all elements greater than the pivot are on the right side. After partitioning, the pivot is in its final sorted position.

3. **Recursively Apply**: Recursively apply the above steps to the sub-arrays of elements with smaller and greater values.

### Steps

Here's a high-level breakdown of the steps involved in Quicksort:

- **Step 1**: Choose a pivot element from the array.
- **Step 2**: Partition the array into two sub-arrays: elements less than the pivot and elements greater than the pivot.
- **Step 3**: Recursively apply Quicksort to the sub-arrays.

### Example

Let's sort the array `[10, 80, 30, 90, 40, 50, 70]` using Quicksort:

- **Initial Array**: `[10, 80, 30, 90, 40, 50, 70]`

1. **Choose Pivot**: Choose `50` as the pivot (could be chosen randomly).

2. **Partitioning**:
   - After partitioning around the pivot `50`, the array might look like `[10, 30, 40, 50, 80, 90, 70]`.
   - Elements less than `50` are on the left (`[10, 30, 40]`), and elements greater than `50` are on the right (`[80, 90, 70]`).

3. **Recursively Sort**:
   - Apply Quicksort recursively to the left sub-array (`[10, 30, 40]`) and the right sub-array (`[80, 90, 70]`).

4. **Final Sorted Array**: After all recursive calls, the array becomes `[10, 30, 40, 50, 70, 80, 90]`.

### Complexity

- **Time Complexity**: 
  - $O(n \log n)$ on average, where $n$ is the number of elements.
  - $O(n^2)$ in the worst-case scenario (rare), typically when the pivot selection is poor (e.g., already sorted array).
- **Space Complexity**: $O(\log n)$ additional space for the recursive call stack.

### Implementation (Python)

Here's a simple implementation of Quicksort in Python:

```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    
    pivot = arr[len(arr) // 2]  # Choosing the middle element as pivot
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    
    return quicksort(left) + middle + quicksort(right)

# Example usage:
arr = [10, 80, 30, 90, 40, 50, 70]
sorted_arr = quicksort(arr)
print("Sorted array:", sorted_arr)
```

In this implementation:
- We recursively partition the array into smaller sub-arrays based on the pivot element.
- Elements less than the pivot go into the left sub-array, equal elements go into the middle sub-array, and greater elements go into the right sub-array.
- We concatenate the sorted left, middle, and right sub-arrays to get the final sorted array.

Quicksort is widely used due to its average-case time complexity of $O(n \log n)$, which makes it suitable for sorting large datasets efficiently. However, care must be taken with its implementation to avoid worst-case scenarios and ensure optimal performance.

MergeSort
---------

Merge Sort is a divide-and-conquer algorithm that divides the input array into smaller sub-arrays, recursively sorts them, and then merges the sorted sub-arrays to produce a final sorted array. It is known for its stable sorting behavior and consistent $O(n \log n)$ time complexity.

### Description

Merge Sort follows these steps:

1. **Divide**: Divide the unsorted array into two halves recursively until each sub-array contains only one element.

2. **Conquer**: Merge the smaller sorted arrays (sub-arrays) back together, ensuring that the merged array remains sorted.

### Steps

Here's a high-level breakdown of how Merge Sort works:

- **Step 1**: Divide the array into two halves.
- **Step 2**: Recursively divide each half until each sub-array contains only one element (base case).
- **Step 3**: Merge the sorted sub-arrays back together:
  - Compare the elements from each sub-array and place them in order in a temporary array.
  - Continue merging until all elements are sorted and merged into a single sorted array.

### Example

Let's sort the array `[38, 27, 43, 3, 9, 82, 10]` using Merge Sort:

- **Initial Array**: `[38, 27, 43, 3, 9, 82, 10]`

1. **Divide**:
   - Divide the array into two halves: `[38, 27, 43, 3]` and `[9, 82, 10]`.

2. **Recursively Sort**:
   - Divide further until each sub-array contains only one element: `[38]`, `[27]`, `[43]`, `[3]`, `[9]`, `[82]`, `[10]`.

3. **Merge**:
   - Merge pairs of sub-arrays:
     - Merge `[38]` and `[27]` to `[27, 38]`.
     - Merge `[43]` and `[3]` to `[3, 43]`.
     - Merge `[9]` and `[82]` to `[9, 82]`.
     - Merge `[10]` with the already merged `[3, 43]` to `[3, 10, 43]`.
   - Merge the remaining sub-arrays until the entire array is sorted: `[3, 9, 10, 27, 38, 43, 82]`.

### Complexity

- **Time Complexity**: $O(n \log n)$ in all cases (worst-case, average-case, and best-case scenarios).
- **Space Complexity**: $O(n)$ additional space for the temporary array used in merging.

### Implementation (Python)

Here's a simple implementation of Merge Sort in Python:

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    
    # Divide the array into two halves
    mid = len(arr) // 2
    left_half = arr[:mid]
    right_half = arr[mid:]
    
    # Recursively sort each half
    left_half = merge_sort(left_half)
    right_half = merge_sort(right_half)
    
    # Merge the sorted halves
    return merge(left_half, right_half)

def merge(left, right):
    sorted_arr = []
    i = j = 0
    
    # Compare elements from left and right sub-arrays
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            sorted_arr.append(left[i])
            i += 1
        else:
            sorted_arr.append(right[j])
            j += 1
    
    # Append remaining elements
    sorted_arr.extend(left[i:])
    sorted_arr.extend(right[j:])
    
    return sorted_arr

# Example usage:
arr = [38, 27, 43, 3, 9, 82, 10]
sorted_arr = merge_sort(arr)
print("Sorted array:", sorted_arr)
```

In this implementation:
- `merge_sort` function recursively divides the array into halves and sorts each half.
- `merge` function merges two sorted arrays (`left` and `right`) into a single sorted array.
- The `merge_sort` function calls `merge` to combine the sorted halves back together to produce the final sorted array.

Merge Sort is efficient and stable, making it a popular choice for sorting large datasets where stability and predictable performance are important considerations.

###Exit Survey

Share this survey for students to fill out: https://docs.google.com/forms/d/e/1FAIpQLScMK2gP-60YXwko2jBmWR6ZzxtrzrGyhIlLM0i-p44D_IVgGw/viewform?usp=sf_link 

###Exam
Reminder that there will be an open-note exam on Friday. This exam is purely for the students to measure their progress and understanding in the class. Whoever scores the highest on the exam will receive a cash prize. 

Exercises
---------

### Quick Sort Exercises

1. **Exercise 1: Implement Quick Sort**
   - **Problem**: Write a function `quick_sort(arr)` that sorts an array `arr` using the Quick Sort algorithm.

2. **Exercise 2: Randomized Pivot Selection**
   - **Problem**: Modify the `quick_sort` function to use a randomly selected pivot to improve performance on average.

3. **Exercise 3: In-place Quick Sort**
   - **Problem**: Implement an in-place version of Quick Sort that sorts the array without using additional memory for new arrays.

### Merge Sort Exercises

1. **Exercise 4: Implement Merge Sort**
   - **Problem**: Write a function `merge_sort(arr)` that sorts an array `arr` using the Merge Sort algorithm.

2. **Exercise 5: Bottom-Up Merge Sort**
   - **Problem**: Implement a bottom-up version of Merge Sort that sorts the array iteratively instead of recursively.

3. **Exercise 6: Merge Sort for Linked List**
   - **Problem**: Implement Merge Sort to sort a singly linked list.
