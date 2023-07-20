---
alias: Bubblesort in Python
tag: python
date: 20-07-2023
---

---

## List Of Contents:

- [[Bubblesort in Python#What is [Bubblesort](https://en.wikipedia.org/wiki/Bubble_sort)? | What is Bubblesort]]
- [[Bubblesort in Python#Bubblesort Procedure/Function Only: | Bubblesort Procedure/Function Only]]
	- [[Bubblesort in Python#Not Optimised: ( Ascending Order ) | Not Optimised: ( Ascending Order )]]
	- [[Bubblesort in Python#Not Optimised ( Desceding Order ): | Not Optimised ( Desceding Order )]]
	- [[Bubblesort in Python#Optimised ( Ascending Order ): | Optimised ( Ascending Order )]]
	- [[Bubblesort in Python#Optimised ( Descending Order ): | Optimised ( Descending Order )]]
- [[Bubblesort in Python#Example ( Unoptimised ): | Example ( Unoptimised )]]
	- [[Bubblesort in Python#Example 1: | Example 1]]

---

# What is [Bubblesort](https://en.wikipedia.org/wiki/Bubble_sort)?

A **bubble sort** also known as a *sinking sort*, is a **simple** algorithm that steps into the array repeatedly.

It will then **compare** each item in the array with one another, then it will swap the items as intended ( ascending / descending order ).

Read more at [Wikipedia](https://en.wikipedia.org/wiki/Bubble_sort)

# Code:

## Bubblesort Procedure/Function Only:

### Not Optimised: ( Ascending Order )

This is the **function** of linear search; it will **not** run on its own.

```python

# Bubblesort Procedure/Function

# We have to pass the array into the procedure/function
# Let our array be called "array" 

def bubble(array):

		# Number of times it will sort the array 
    for x in range(0, len(array) - 1):

				# Checks every value in array
        for y in range(0, len(array) - 1):

						# Ascending Order
            if array[y] > array[y + 1]:

								# Swapping part of algorithm
                temp = array[y]
                array[y] = array[y + 1]
                array[y + 1] = temp

```

### Not Optimised ( Desceding Order ):

```python

# Bubblesort Procedure/Function

# We have to pass the array into the procedure/function
# Let our array be called "array" 

def bubble(array):

		# Number of times it will sort the array
    for x in range(0, len(array) - 1):

				# Checks every value in array
        for y in range(0, len(array) - 1):

						# Descending Order
            if array[y] < array[y + 1]:

								# Swapping part of algorithm
                temp = array[y]
                array[y] = array[y + 1]
                array[y + 1] = temp

```

### Optimised ( Ascending Order ):

```python



```

### Optimised ( Descending Order ):

```python



```

# Example ( Unoptimised ):

## Example 1:

```python

# Array with identifer name "array" with size = infinite
array = []

print()

# Exception Handling
try:

    # Asking the user to input the size of the array
    array_size = int(input("Please Enter Size Of Array: "))

# If user inputs a character other than an Integer
except ValueError:

    # Display appropriate message
    print("Please Enter Whole Numbers Only!")

print()

# Exception Handling
try:

    # Asking the user to input data into the array
    for count in range(array_size):
  
        user_input = int(input("Please Enter A Value: "))

        # Appending data that user entered into the array
        array.append(user_input)

# If user inputs a character other than an Integer
except ValueError:

    # Display appropriate message
    print("Please Enter Whole Numbers Only!")

print()
# Displaying array BEFORE bubblesort
print("Array Before Bubblesort: ")
print()

# Displaying array with data in separate lines
for index in array:

    print(index)

# Function/Procedure "bubble"
# "array is passed"
def bubble(array):

    # Number of times it will sort the array
    for x in range(0, len(array) - 1):

        # Checks every value in array
        for y in range(0, len(array) - 1):

            # Ascending Order
            if array[y] > array[y + 1]:

                # Swapping part of algorithm
                temp = array[y]
                array[y] = array[y + 1]
                array[y + 1] = temp

# Calling the Function/Procedure "bubble"
bubble(array)

print()
# Displaying array AFTER bubblesort
print("Array After Bubblesort: ")
print()

# Displaying array with data in separate lines
for j in array:

    print(j)

```