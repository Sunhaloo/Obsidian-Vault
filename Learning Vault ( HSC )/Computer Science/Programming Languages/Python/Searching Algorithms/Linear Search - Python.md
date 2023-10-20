---
Alias: Linear Search In Python
Tag: python, searching_algo
Author: S.Sunhaloo
Type: Searching Algorithm
Date: 2023-09-13
Status: Waiting 2D Array
---

## List of Contents

- [[Linear Search - Python#What is a Linear Search? | What is a Linear Search?]]

---
## Linear Search

## [[Arrays - Python#One Dimensional Arrays ( 1D-Arrays ) | One Dimensional Arrays]]

- [[Linear Search - Python#Linear Search Code - 1D Array| Linear Search Code]]
	- [[Linear Search - Python#Template | Template Function]]
	- [[Linear Search - Python#Examples | Examples]]

---

## [[Arrays - Python#Two Dimensional Arrays ( 2D-Arrays ) | Two Dimensional Arrays]]

---

My Links

- [[Linear Search - Python#Socials | Links to Socials]]

---

# [[Arrays - Python#One Dimensional Arrays ( 1D-Arrays ) | One Dimensional Arrays]]

# What is a Linear Search?

This is one of the simplest [[Python Data View#Searching Algorithms | searching algorithm]]. This is because it searches the array **sequentially**. In fact, the another name for linear search is *sequential search*.

In linear search the array **does not** need to be *sorted*.

The *calculation* of linear search is written below:

1. We have to calculate the **length** of *array*
2. There is a ( "*for*" )  loop which will step through the array
	- If the **value** at that *address* is found
		- It returns the **address** of the value
3. If value has **not** been found it exits the loop
	- By return *-1* or *False*

# Some Advantages

- Very easy to implement in code
- Fast on ( and only one ) small arrays
- The array does not need to be sorted
- Linear Search if not affected by the data movement
	- Data being:
		- Added to array
		- Removed from array

# Some Disadvantages

- Very slow for large data sets ( arrays )
	- Because it searches the array sequentially

> For more advantages and disadvantages; just [Google](https://google.com) them. The thing is that you need to know is:
> - Understand how it works
> - The actually program code

# Linear Search Code - 1D Array

## Template

This is only the [[Functions and Procedures - Python#Example 4 Linear Search| function]], thus is will **not** run on its own.

```python

# Linear Search Function

# Function with identifier name "linear_search"

# In this function we need to pass the:
# array
# search value ( user_find )
def linear_search(array, user_find):

    # Loop steps through array
    for i in range(0, len(array)):

        # If value is found
        if array[i] == user_find:

            # Returns the address of "user_find"
            return i

    # If search value has not been found
    return -1

```

## Examples:

### Example 1: Complete Code

```python

# Linear Search

print()

# Array with identifier name "numbers"
numbers = []

# Asking the user to enter the size of the array "numbers"

# Exception Handling
try:

    # Variable "array_size" will hold the "size of the array"
    print()
    array_size = int(input("Please Enter Size Of Array: "))
    print()

# If user enter any character other than Integers
except ValueError:

    # Outputs appropriate message
    print()
    print("Please Enter Integer Values Only!")
    print()

# Asking the user to enter data into array
for x in range(array_size):

    # Asking the user to enter a value
    user_input = input("Please Enter A Number: ")

    # Check if user_input is a digit
    if user_input.isdigit():

        # If "user_input" is an integer
        # "user_input" will be converted to Integer
        user_input = int(user_input)

    # If user does not input Integers
    else:

        # Ouptputs appropriate message
        print("Please Enter Whole Numbers Only!")

    # When "user_input" is of type Integer
    # Appends the value to the array
    numbers.append(user_input)

# Variable "user_find" will hold serach value
print()
user_find = input("Please Enter A Number To Find: ")
print()

# If search value is an integer
if user_find.isdigit():

    # "user_find" will be converted to Integer
    user_find = int(user_find)

# If user did not enter an integer number
else:

    # Outputs appropriate message
    print("Please Enter Whole Numbers Only!")

# Linear Search Function:
def linear_search(numbers, user_find):

    # Loop steps through array
    for i in range(0, len(numbers)):

        # If value is found
        if numbers[i] == user_find:

            # Returns the address of "user_find"
            return i

    # If search value has not been found
    return -1

# Calling Function
search_value = linear_search(numbers, user_find)

# Displaying search_value
print(search_value)

```

# [[Arrays - Python#Two Dimensional Arrays ( 2D-Arrays ) | Two Dimensional Arrays]]

---

# Socials

- [**Instagram:**](https://www.instagram.com/s.sunhaloo/)
- [**YouTube:**](https://www.youtube.com/@s.sunhaloo539/streams)

---
Thank You!