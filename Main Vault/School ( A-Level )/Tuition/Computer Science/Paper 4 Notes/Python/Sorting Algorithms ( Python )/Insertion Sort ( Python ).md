---
alias: Insertion Sort ( Python )
tag: python
date: 07-08-2023
---

---

## List Of Contents:

- [[Insertion Sort ( Python )#What is [Insertion Sort](https //en.wikipedia.org/wiki/Insertion_sort)? | What is Insertion Sort?]]
- [[Insertion Sort ( Python )#Advantages of Insertion Sort | Advantages of Insertion Sort]]
- [[Insertion Sort ( Python )#Disadvantages of Insertion Sort | Disadvantages of Insertion Sort]]

---

# What is [Insertion Sort](https://en.wikipedia.org/wiki/Insertion_sort)?

 It is a **simple** [[Python Road-Map#Sorting Algorithms | sorting algorithm]] that sorts an array one element at a time. This is done by comparisons, i.e we compare 2 elements to each other in the array until it is sorted.

# Advantages of Insertion Sort:

- It is **easy** to implement
- Efficient with **small** data set/arrays
- **More efficient** than *[[Bubble Sort ( Python )| Bubble Sort]]*
- Can sort data as it receives it

# Disadvantages of Insertion Sort:

- **Not efficient** on *large* data set
- Does not perform well compared to more advanced sorting algorithms

# Insertion Sort Code

# Insertion Sort Function

## Ascending Order

This is the function only; it will **not** run on its on.

```python

# Insertion Sort

# Function with identifier name "insertion_sort"
# It will take 1 argument, i.e our array
def insertion_sort(array):

    # Calculate length of array
    length_array = len(array)

    # "for" loop that starts at index 1 instead of 0
    for i in range(1, length_array):

        # Values at address "i"
        values = array[i]

        # Values to the left of "i" (  one before "i")
        j = i - 1

        # Condition to enter "while" loop
        while j >= 0 and array[j] > values:

            # Sorting Part
            # Swapping values
            array[j + 1] = array[j]

            # Decrease "j" by 1
            j = j - 1
            
        # Already sorted
        array[j + 1] = values

```

## Descending Order

```python

# Insertion Sort

# Function with identifier name "insertion_sort"
# It will take 1 argument, i.e our array
def insertion_sort(array):

    # Calculate length of array
    length_array = len(array)

    # "for" loop that starts at index 1 instead of 0
    for i in range(1, length_array):

        # Values at address "i"
        values = array[i]

        # Values to the left of "i" (  one before "i")
        j = i - 1

        # Condition to enter "while" loop
        while j >= 0 and array[j] < values:

            # Sorting Part
            # Swapping values
            array[j + 1] = array[j]

            # Decrease "j" by 1
            j = j - 1
            
        # Already sorted
        array[j + 1] = values

```

>[!note]
>Insertion sort is **not** like [[Bubble Sort ( Python )| Bubble Sort]].
> - Bubble Sort with take element at index **0** and compares it to element at index **1**;
> While Insertion Sort will 
> - **Starts** with the element at index **1** ( *second element* ) and then compares it with element at index **0** ( *first element* )
> **Meaning:** Anything to the left hand side of the pointer "i" is a sorted array

# Example:

This code will sort an array with values already in it in ascending order.

```python

# Insertion Sort

# Array with identifier name "array"
array = [11, 9, 29, 7, 2, 15, 28]

# Function with identifier name "insertion_sort"
# It will take 1 argument, i.e our array
def insertion_sort(array):

    # Calculate length of array
    length_array = len(array)

    # "for" loop that starts at index 1 instead of 0
    for i in range(1, length_array):

        # Values at address "i"
        values = array[i]

        # Values to the left of "i" (  one before "i")
        j = i - 1

        # Condition to enter "while" loop
        while j >= 0 and array[j] < values:

            # Sorting Part
            # Swapping values
            array[j + 1] = array[j]
            
            # Decrease "j" by 1
            j = j - 1

        # Already sorted
        array[j + 1] = values

# Calling Functions
insertion_sort(array)

# Displaying Array
for count in array:

    # Outputs values on separate lines
    print(count)

```
