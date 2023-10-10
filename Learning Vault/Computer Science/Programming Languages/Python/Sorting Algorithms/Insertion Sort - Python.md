---
Alias: Insertion Sort ( Simpler Sorting Algo )
Tag: python, sorting_algo
Author: S.Sunhaloo
Type: Sorting Algorithm
Date: 01-09-2023
Status: Waiting 2D Array
---

## List of Contents

## [[Arrays - Python#One Dimensional Arrays ( 1D-Arrays ) | One Dimensional Array]]

- [[Insertion Sort - Python#What is Insertion Sort? | What is Insertion Sort?]]
	- [[Insertion Sort - Python#Some advantages | Advantages]]
	- [[Insertion Sort - Python#Some Disadvantages | Disadvantages]]
- [[Insertion Sort - Python#Insertion Sort Code - 1D Array | Insertion Sort Code - 1D Array]]
	- [[Insertion Sort - Python#Template | Template]]
- [[Insertion Sort - Python#Example | Example]]
	- [[Insertion Sort - Python#Example 1 Complete Code | Complete Code]]

---

## [[Arrays - Python#Two Dimensional Arrays ( 2D-Arrays ) | Two Dimensional Array]]

---

My Links

- [[Insertion Sort - Python#Socials | Links to Social]]

---

# What is Insertion Sort?

This is another [[Python Data View#Sorting Algorithms ( 2D and 1D Array ) | sorting algorithm]] that is works well if programmer need to find a value quickly.

The *calculation* of Insertion Sort is as follow:

1. It will find the **length** of array
2. There is a variable which will hold:
	- The **value** at *index* "*x*"
3. Another variable will hold the value at:
	- "*x + 1*"
4. It compares the second value to the first value
	- Then swap accordingly ( ascending / descending order )

# Some advantages

- It is easy and faster to implement
	- Because lines of code is less than bubble sort
- More efficient than bubble sort
- Can sort data as it receives it

# Some Disadvantages

- Slow on large data set ( arrays )
- Does not perform well compared to more advanced sorting algorithms

# Insertion Sort Code - 1D Array

## Template

This is only the [[Functions and Procedures - Python#Example 2 Insertion Sort| function]], thus is will **not** run on its own.

```python

# Insertion Sort Function

# Function with identifier name "insertion_sort"

# In this function. we need to pass:
# array
def insertion_sort(array):

    # Calculates length of array
    length_array = len(array)

    # "for" loop that starts at index 1 instead of 0
    for i in range(1, length_array):

        # Values at address "i"
        values = array[i]

        # Values to the left of "i" (  one before "i")
        j = i - 1

        # Condition to enter "while" loop
        while j >= 0 and array[j] > values:

            # Swapping Part
            array[j + 1] = array[j]

            # Decrease "j" by 1
            j = j - 1

        # If array is already sorted
        array[j + 1] = values

```

>See it's really simple, that is why is is really easy to implement into code as the number of lines is oh so little

## Example

### Example 1: Complete Code

```python

# Insertion Sort

# Array with identifier name "array"
array = [11, 9, 29, 7, 2, 15, 28]

# Function with identifier name "insertion_sort"

# In this function. we need to pass:
# array
def insertion_sort(array):

    # Calculates length of array
    length_array = len(array)

    # "for" loop that starts at index 1 instead of 0
    for i in range(1, length_array):

        # Values at address "i"
        values = array[i]

        # Values to the left of "i" (  one before "i")
        j = i - 1

        # Condition to enter "while" loop
        while j >= 0 and array[j] > values:

            # Swapping Part
            array[j + 1] = array[j]

            # Decrease "j" by 1
            j = j - 1

        # If array is already sorted
        array[j + 1] = values

# Calling Functions
insertion_sort(array)

# Displaying Array
for count in array:

    # Output all the values of array on separate lines
    print(count)

```

# [[Arrays - Python#Two Dimensional Arrays ( 2D-Arrays ) | Two Dimensional Array]]

---

# Socials

- [**Instagram:**](https://www.instagram.com/s.sunhaloo/)
- [**YouTube:**](https://www.youtube.com/@s.sunhaloo539/streams)

---
Thank You!