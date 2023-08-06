---
alias: Bubblesort in Python
tag: python
date: 20-07-2023
---

---

## List Of Contents:

- [[Bubblesort  Python#What is [Bubblesort](https://en.wikipedia.org/wiki/Bubble_sort)?| What is Bubblesort]]
- [[Bubblesort  Python#Bubblesort Procedure/Function Only:| Bubblesort Procedure/Function Only]]
	- [[Bubblesort  Python#Not Optimised: ( Ascending Order )| Not Optimised: ( Ascending Order )]]
	- [[Bubblesort  Python#Not Optimised ( Desceding Order ):| Not Optimised ( Desceding Order )]]
	- [[Bubblesort  Python#Optimised ( Ascending Order ):| Optimised ( Ascending Order )]]
	- [[Bubblesort  Python#Optimised ( Descending Order ):| Optimised ( Descending Order )]]
- [[Bubblesort  Python#Examples ( Unoptimised ):| Examples ( Unoptimised )]]
- [[Bubblesort  Python#Examples ( Optimised ):| Examples ( Optimised) ]]

---

# What is [Bubblesort](https://en.wikipedia.org/wiki/Bubble_sort)?

A **bubble sort** also known as a *sinking sort*, is a **simple** algorithm that steps into the array repeatedly.

It will then **compare** each item in the array with one another, then it will swap the items as intended ( ascending / descending order ).

# Code:

## Bubblesort Procedure/Function Only:

### Not Optimised: ( Ascending Order )

This is the **function** of linear search; it will **not** run on its own.

```python

# Bubblesort Procedure/Function ( NOT Optimised )

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

This is the **function** of linear search; it will **not** run on its own.

```python

# Bubblesort Procedure/Function ( NOT Optimised )

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

This is the **function** of linear search; it will **not** run on its own.

```python

# Bubblesort Procedure/Function ( Optimised )

# We have to pass the array into the procedure/function
# Let our array be called "array" 

def bubblesort_optimised(array):

		# We will have some other variables

		# "update" will check if the value has moved from original place
    update = True

		# "swaps" will keep track of the number of times that value has been swapped
    swaps = 0

		# Conditin to enter while loop
    while update == True and len(array) > 1:


        update = False

				# Number of times it will sort the array
        for x in range(0, len(array) - 1):

						# Checks every value in array
            for y in range(0, len(array) - 1):


                if array[y] > array[y +1]:

										# Swapping part of algorithm
                    temp = array[y]
                    array[y] = array[y + 1]
                    array[y + 1] = temp
                    
                    swaps += 1
                    update =True
                    
    return array, swaps

```

### Optimised ( Descending Order ):

This is the **function** of linear search; it will **not** run on its own.

```python

# Bubblesort Procedure/Function ( Optimised )

# We have to pass the array into the procedure/function
# Let our array be called "array" 

def bubblesort_optimised(array):

		# We will have some other variables

		# "update" will check if the value has moved from original place
    update = True

		# "swaps" will keep track of the number of times that value has been swapped
    swaps = 0

		# Conditin to enter while loop
    while update == True and len(array) > 1:


        update = False

				# Number of times it will sort the array
        for x in range(0, len(array) - 1):

						# Checks every value in array
            for y in range(0, len(array) - 1):


                if array[y] < array[y +1]:

										# Swapping part of algorithm
                    temp = array[y]
                    array[y] = array[y + 1]
                    array[y + 1] = temp
                    
                    swaps += 1
                    update =True
                    
    return array, swaps


```

# Examples ( Unoptimised ):

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

# Examples ( Optimised ):

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

# Function/Procedure "bubble_optimised"
# "array is passed"
def bubble_optimised(array):

		# We will have some other variables

		# "update" will check if the value has moved from original place
    update = True

		# "swaps" will keep track of the number of times that value has been swapped
    swaps = 0

		# Conditin to enter while loop
    while update == True and len(array) > 1:


        update = False

				# Number of times it will sort the array
        for x in range(0, len(array) - 1):

						# Checks every value in array
            for y in range(0, len(array) - 1):


                if array[y] > array[y +1]:

										# Swapping part of algorithm
                    temp = array[y]
                    array[y] = array[y + 1]
                    array[y + 1] = temp
                    
                    swaps += 1
                    update =True
                    
    return array, swaps

result = bubble_optimised(array)

# Note that I do not know how to make it print each element on different lines
print(result)

```

---
S.Sunhaloo