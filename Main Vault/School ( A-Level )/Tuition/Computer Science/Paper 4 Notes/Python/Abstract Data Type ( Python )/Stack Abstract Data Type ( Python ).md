---
alias: Stack Abstract Data Type ( Python )
tag: python
date: 04-08-2023
---

---

# List Of Contents

- [[Stack Abstract Data Type ( Python )#What is a [Stack](https //en.wikipedia.org/wiki/Stack_(abstract_data_type) ~ text=In%20computer%20science%2C%20a%20stack,that%20was%20not%20yet%20removed.)? | What is a Stack?]]
- [[Stack Abstract Data Type ( Python )#Stack Program Code | Stack Program Code]]
	- [[Stack Abstract Data Type ( Python )#Functions | Functions]]
		- [[Stack Abstract Data Type ( Python )#Implementing Array for Stack | Implementing Array for Stack]]
		- [[Stack Abstract Data Type ( Python )#Display Array | Display Array]]
		- [[Stack Abstract Data Type ( Python )#Insert Values | Insert Values]]
		- [[Stack Abstract Data Type ( Python )#POP Operation | POP Operation]]
		- [[Stack Abstract Data Type ( Python )#Delete Item by User | User tells what to delete]]
		- [[Stack Abstract Data Type ( Python )#Bubble Sort | Bubble Sort]]
		- [[Stack Abstract Data Type ( Python )#Linear Search Code | Linear Search Code]]
			- [[Stack Abstract Data Type ( Python )#Calling and Displaying the values of the function ( Linear Search ) | Outputs the Linear Search result in a "good-looking manner"]]
		- [[Stack Abstract Data Type ( Python )#Binary Search | Binary Search]]
			- [[Stack Abstract Data Type ( Python )#Binary Search Code | Code For Binary Search]]
		- [[Stack Abstract Data Type ( Python )#Calling and Displaying the values of the function ( Binary Search ) | Outputs the Binary Search result in a "good-looking manner"]]
- [[Stack Abstract Data Type ( Python )#Example Of Stack Code | Example Of Stack Program Code]]

---

# What is a [Stack](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)#:~:text=In%20computer%20science%2C%20a%20stack,that%20was%20not%20yet%20removed.)?

It is an [[Abstract Data Types ( Python ) | abstract data type]] that serves as a collection of elements with 2 main **operations**:

- PUSH:
	- To **add** or **insert** an item into the stack/array
- POP:
	- To **remove** or **delete** an item into the stack/array

---

To understand **stack data structure**; we need to think of it as a *stack of plates*. Picture a stack of plate in your head, try to think that the *plate is a data item*

Now, if we would like to **add**/**insert** a plate into the *stack*; a sane person would *place*/*add* the new plate on top

- This is how the **PUSH** operation works, it adds new items in to the stack/array *at* the **top**

Now, if we would like to **remove**/**delete**, a plate from the *stack*; a sane person would *remove* a plate from the top

- This is how the **POP** operation works, it removes the **last** item *from* the **top**

---

# Stack Program Code

## Functions

To implement a stack, we will need to use an [[Arrays in Python | array]] and for this program code I will break it down its [[Functions | functions]]

## Implementing Array for Stack

```python

# Stack Program Code

# Array with identifier name "array" and size = undefined
array = []

```

## Display Array 

This is a function that will be used to display the data values on each line.

```python

# Stack Program Code

# Function with identifier name "display_array"
def display_array():

    # If array is empty
    if not array:

        print()
        # Outputs Appropriate Message
        print("There is nothing in the array!")
        print()

    # If array is not empty
    else:

        # Loop to step through array
        for count in array:

            # Display each item on seperate lines
            print(count)

```

## Insert Values

This is a function what will be used to allow a user to enter data into the stack/array.

```python

# Stack Program Code

# Function with identifier name "insert_value"
def insert_value():

    # Exception Handling
    try:

        # Variable to hold user desired array size
        array_size = int(input("Please enter size of array: "))

    # If user does not input integer values
    except ValueError:

        # Outputs appropriate message
        print("Please Enter Integer Values Only!")

    # Exception Handling
    try:    

        # Loop to go through array
        for x in range(array_size):

            # Variable that will hold the value entered by user
            user_input = int(input("Please enter a value: "))

            # Adds "user_input" to array
            array.append(user_input)

    # If user does not input integer values
    except ValueError:

       # Outputs appropriate message
       print("Please Enter Integer Values Only")

```

## POP Operation

This function will be used to remove the last item of the array.

```python

# Stack Program Code

# Function with identifier name "pop"
def pop_last():

    # Remove last item from array
    array.pop()

```

## Delete Item by User

This function will allow the user to enter an item, it will then:

- Step through the array
- Finds the data at the specific location
- Remove the data
- Else
	- Does not remove anything

### With "While Loop"

```python

# Stack Program Code

# Function with identifier name "remove_value_user"
def remove_value_user():

  # Variable "found" is of type boolean
  found = False

  # Exception Handling
  try:

  # Ask the user to enter a value to find
    user_input_remove = int(input("Please Enter A Value To Remove: "))

  except ValueError:

    # Outputs this message
    print("Please Enter Integer Values Only")

  # Condition to enter "while" loop
  while not found:

    # Variable "count" that will step through the array
    for count in array:

      # If value at "count" is equal to value to be removed
      if count == user_input_remove:

        # It removes the value
        array.remove(count)

        # "found" becomes "True" as it indicates that value has been removed
        found = True

    # If the value to be removed is not in array
    if count != user_input_remove:
    
      # Outputs appropriate message

      print(str(user_input_remove) + " has not been found!")
      break

```

### With "For Loop"

```python

# Stack Program Code

# Function with identifier name "remove_value_user"
def remove_value_user():

    # Exception Handling
    try:

        # Ask the user to enter a value to find
        user_input_remove = int(input("Please Enter A Value To Remove: "))

    except ValueError:

        # Outputs this message
        print("Please Enter Integer Values Only")

    # Variable "count" that will step trough array
    for count in array:

        # If value at "count" is equal to value to be removed
        if count == user_input_remove:

            # It removes the value
            array.remove(count)

    # If the value removed is not in array
    if count != user_input_remove:

        # Outputs appropriate message
        print(str(user_input_remove) + " has not been found!")
        break

```

## Bubble Sort

This function will sort the array. The sorting may be in:

1. Ascending Order
2. Descending Order

### Ascending Order

```python

# Stack Program Code

# Function with identifier name "bubblesort"
# This is an "OPTIMISED" version of bubblesort
# If the user wants to use the variables "update" and "swaps"
    # He just needs to add "return update, swaps"
def bubblesort():

    #Calculate length of array
    array_length = len(array)

    # Variable to tell us that if values has been updated
    update = True

    # Variable to tell us how many times values has been swapped
    swap = 0

    # Condition to enter "while" loop
    while update == True and array_length > 1:

        # update needs to be "FALSE" to be able to tell that user that the array has been update
        update = False

        # Number of times it will sort the array
        for x in range(0, array_length - 1):

            # Checks for every value in the array
            for y in range(0, array_length - 1):

                # Sorting in Ascending Order
                if array[y] > array[y + 1]:

                    # Sorting part of algorithm
                    temp = array[y]
                    array[y] = array[y + 1]
                    array[y + 1] = temp

                    # "update" becomes TRUE
                    update = True

                    # "swap" increases by one
                    swap += 1

```

### Descending Order

```python

# Stack Program Code

# Function with identifier name "bubblesort"
# This is an "OPTIMISED" version of bubblesort
# If the user wants to use the variables "update" and "swaps"
    # He just needs to add "return update, swaps"
def bubblesort():

    #Calculate length of array
    array_length = len(array)

    # Variable to tell us that if values has been updated
    update = True

    # Variable to tell us how many times values has been swapped
    swap = 0

    # Condition to enter "while" loop
    while update == True and array_length > 1:

        # update needs to be "FALSE" to be able to tell that user that the array has been update
        update = False

        # Number of times it will sort the array
        for x in range(0, array_length - 1):

            # Checks for every value in the array
            for y in range(0, array_length - 1):

                # Sorting in Descending Order
                if array[y] < array[y + 1]:

                    # Sorting part of algorithm
                    temp = array[y]
                    array[y] = array[y + 1]
                    array[y + 1] = temp

                    # "update" becomes TRUE
                    update = True

                    # "swap" increases by one
                    swap += 1

```

## Linear Search

This will allow one to search values inside of the stack/array.

### Linear Search Code

```python

# Stack Program Code

# Function with identifier name "linear_search"
# Two arguements have been passed inside the function
    # We need to pass the array and the value to find
    # In this case our array has the identifier name "array"
    # In this case our value to search has the identifier name "user_linear_find"
def linear_search(array, user_linear_search):

    # Calculating the length of the array
    length_array_linear = len(array)

    # Loop to step through array
    for x in range(0, length_array_linear):

        # If value at index/address "x" is equal to value to find
        if array[x] == user_linear_search:

            # Return the address of the data
            return x

    # Else it will return False
    return -1

```

### Calling and Displaying the values of the function ( Linear Search )

This will display the function ( Linear Search ) in an appropriate manner.

> This is how I would have called and display the array

```python

# Stack Program Code

# Returning the result in an appropriate manner
result = linear_search(array, user_linear_search)

# Displaying
  
# If statement to know what to print
# NOTE: To be able to use this code, we need to return "-1" instead of "False"
if result != -1:

    # Outputs - if value has been found
    print(str(user_linear_search) + " has been found at: " + str(result))

else:

    # Outputs - if value has not been found
    print(str(user_linear_search) + " has not been found!")

```

## Binary Search

This will allow a person to search for the values inside of the stack/array

### Binary Search Code

>[!note]- 
>This is **not** the *recursive* binary search code
> [[Binary Search Python#Binary Search Recursive Function| Click Here]] to view the binary search code for the **recursive one**

```python

# Stack Program Code

# Function with identifier name "binary_search"
# 2 arguments have been passed into the function
def binary_search(array, user_binary_search):

    # Function return the calculation part of the Binary Search
    return binary_search_calculation(array, 0 , len(array) -1, user_binary_search)

# Function with identifier name "binar_search_calc"
# 4 arguments have been passed into the function
def binary_search_calculation(array, lower, upper, user_binary_search):

    # Condition to enter "while" loop
    while lower <= upper:

        # Calculating the middle of array
        mid = (lower + upper) // 2

        # If middle value is equal to value to be searched
        if array[mid] == user_binary_search:

            # Return address of value
            return mid

        # If value to be searched is found in the upper part of the array
        # In short this cuts the array in half
        elif array[mid] < user_binary_search:

            # Variable "lower" take the position one value after the middle value
            lower = mid + 1
            
        else:

            # If value to be searched is found in the upper part of the array
            # Variable "upper" take the position one value before them middle of array
            upper = mid - 1

    # If Value has not been found
    return -1

```

### Calling and Displaying the values of the function ( Binary Search )

This will display the function ( Binary Search ) in an appropriate manner.

> This is how I would have called and display the array

```python

# Stack Program Code

# Returning the result in an appropriate manner
result = binary_search(array, user_binary_search)

# Displaying
  
# If statement to know what to print
# NOTE: To be able to use this code, we need to return "-1" instead of "False"
if result != -1:

    # Outputs - if value has been found
    print(str(user_binary_search) + " has been found at: " + str(result))

else:

    # Outputs - if value has not been found
    print(str(user_binary_search) + " has not been found!")

```
# Example Of Stack Code:

>[!tip] Full Stack Code

```python

# Stack Program Code

# Array with identifier name "array" and size = undefined
array = []

# Function with identifier name "display_array"
def display_array():

  # If array is empty
  if not array:

    print()
    # Outputs Appropriate Message
    print("There is nothing in the array!")
    print()

  # If array is not empty
  else:

    # Loop to step through array
    for i in array:
    
      # Display each item on seperate lines
      print(i)

# Function with identifier name "insert_value"
def insert_value():

  # Exception Handling
  try:

    # Variable to hold user desired array size
    array_size = int(input("Please enter size of array: "))

  # If user does not input integer values
  except ValueError:

    # Outputs appropriate message
    print("Please Enter Integer Values Only!")

  # Exception Handling
  try:  

    # Loop to go through array
    for x in range(array_size):

      # Variable that will hold the value entered by user
      user_input = int(input("Please enter a value: "))

      # Adds "user_input" to array
      array.append(user_input)

  # If user does not input integer values
  except ValueError:

   # Outputs appropriate message
   print("Please Enter Integer Values Only")

# Function with identifier name "pop"
def pop_last():

  # Remove last item from array
  array.pop()
  
# Function with identifier name "remove_value_user"
def remove_value_user():

  # Variable "found" is of type boolean
  found = False
  
  # Exception Handling
  try:
  
  # Ask the user to enter a value to find
    user_input_remove = int(input("Please Enter A Value To Remove: "))

  except ValueError:
  
    # Outputs this message
    print("Please Enter Integer Values Only")

  # Condition to enter "while" loop
  while not found:

    # Variable "count" that will step through the array
    for count in array:

      # If value at "count" is equal to value to be removed
      if count == user_input_remove:

        # It removes the value
        array.remove(count)

        # "found" becomes "True" as it indicates that value has been removed
        found = True

    # If the value to be removed is not in array
    if count != user_input_remove:

      # Outputs appropriate message
      print(str(user_input_remove) + " has not been found!")
      break

# Function with identifier name "bubblesort"
# This is an "OPTIMISED" version of bubblesort
# If the user wants to use the variables "update" and "swaps"
  # He just needs to add "return update, swaps"
def bubblesort():

  #Calculate length of array
  array_length = len(array)

  # Variable to tell us that if values has been updated
  update = True

  # Variable to tell us how many times values has been swapped
  swap = 0

  # Condition to enter "while" loop
  while update == True and array_length > 1:

    # update needs to be "FALSE" to be able to tell that user that the array has been update
    update = False

    # Number of times it will sort the array
    for x in range(0, array_length - 1):

      # Checks for every value in the array
      for y in range(0, array_length - 1):

        # Sorting in Ascending Order
        if array[y] > array[y + 1]:

          # Sorting part of algorithm
          temp = array[y]
          array[y] = array[y + 1]
          array[y + 1] = temp

          # "update" becomes TRUE
          update = True

          # "swap" increases by one
          swap += 1

# Function with identifier name "linear_search"
# Two arguements have been passed inside the function
  # We need to pass the array and the value to find
  # In this case our array has the identifier name "array"
  # In this case our value to search has the identifier name "user_linear_find"
def linear_search(array, user_linear_search):

  # Calculating the length of the array
  length_array_linear = len(array)

  # Loop to step through array
  for x in range(0, length_array_linear):

    # If value at index/address "x" is equal to value to find
    if array[x] == user_linear_search:

      # Return the address of the data
      return x

  # Else it will return False
  return -1
  
# Function with identifier name "binary_search"
# 2 arguments have been passed into the function
def binary_search(array, user_binary_search):

  # Function return the calculation part of the Binary Search
  return binary_search_calculation(array, 0 , len(array) -1, user_binary_search)

# Function with identifier name "binar_search_calc"
# 4 arguments have been passed into the function
def binary_search_calculation(array, lower, upper, user_binary_search):
  
  # Condition to enter "while" loop
  while lower <= upper:

    # Calculating the middle of array
    mid = (lower + upper) // 2

    # If middle value is equal to value to be searched
    if array[mid] == user_binary_search:
    
      # Return address of value
      return mid

    # If value to be searched is found in the upper part of the array
    # In short this cuts the array in half
    elif array[mid] < user_binary_search:

      # Variable "lower" take the position one value after the middle value
      lower = mid + 1

    else:

      # If value to be searched is found in the upper part of the array
      # Variable "upper" take the position one value before them middle of array
      upper = mid - 1

  # If Value has not been found
  return -1

# Calling Functions
print()

print("Displaying Array")

display_array()

print()

print("Insert Values Into Array")

print()

insert_value()

print()

print("Displaying Array After Inserting Values")

print()

display_array()

print()

print("Removing Last Value")

pop_last()

print()

print("Displaying Array After Removing Last Value From Array")

print()

display_array()

print()

print("Ask User To Remove A Value From Array")

print()

remove_value_user()

print()

print("Displaying Array After User Has Removed")

print()

display_array()

print()

bubblesort()

print("Displaying Array AFTER Bubble Sort")

print()

display_array()

print()

print("Linear Search")

print()

# Ask the user to enter a value to find
# Exception Handling
try:

  user_linear_search = int(input("Please Enter A Value To Search: "))

# If user enter a non-integer value
except ValueError:

  # Outputs appropriate message
  print("Please Enter Integer Values Only")

print()

# Making the output more appropriate
# Returning the result in an appropriate manner
result_linear = linear_search(array, user_linear_search)

# NOTE: To be able to use this code, we need to return "-1" instead of "False"
# If statement to know what to print
if result_linear != -1:

  # Outputs - if value has been found
  print(str(user_linear_search) + " has been found at: " + str(result_linear))

else:

  # Outputs - if value has not been found
  print(str(user_linear_search) + " has not been found!")

print()

print("Binary Search")

print()

# Ask the user to enter a value to find
# Exception Handling
try:

  user_binary_search = int(input("Please Enter A Value To Search: "))

# If user enter a non-integer value
except ValueError:
  # Outputs appropriate message

  print("Please Enter Integer Values Only")

print()

# Making the output more appropriate
# Returning the result in an appropriate manner
result_binary = binary_search(array, user_binary_search)

# If statement to know what to print
# NOTE: To be able to use this code, we need to return "-1" instead of "False"
if result_binary != -1:

  # Outputs- if value has been found
  print(str(user_binary_search) + " has been found at: " + str(result_binary))

else:

  # Outputs- if value has not been found
  print(str(user_binary_search) + " has not been found!")

print()

```

---
S.Sunhaloo