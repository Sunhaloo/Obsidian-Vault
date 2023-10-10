---
Alias: Binary Search In Python
Tag: python, searching_algo
Author: S.Sunhaloo
Type: Searching Algorithm
Date: 13-09-2023
Status: Waiting 2D Array
---

## List of Contents:

- [[Binary Search - Python#What is Binary Search? | What is Binary Search?]]

## Binary Search

 ## [[Arrays - Python#One Dimensional Arrays ( 1D-Arrays ) | One Dimensional Arrays]]

- [[Binary Search - Python#Binary Search Code - 1D Array| Binary Search Code - 1D Array]]
	- [[Binary Search - Python#Template | Function Template ( Non-Recursive )]]
	- [[Binary Search - Python#Examples ( Non-Recursive ) | Examples]]

## Binary Search Recursive

- [[Binary Search - Python#Binary Search Recursive Code - 1D Array| Binary Search Recursive Code]]
	- [[Binary Search - Python#Template - 1D Array ( RECUSIVE )| Function Template ( Recursive )]]
	- [[Binary Search - Python#Examples ( Recursive ) | Examples]]

---

## [[Arrays - Python#Two Dimensional Arrays ( 2D-Arrays ) | Two Dimensional Arrays]]

---

### My Links

- [[Binary Search - Python#Socials | Links to Socials]]

---

 # [[Arrays - Python#One Dimensional Arrays ( 1D-Arrays ) | One Dimensional Arrays]]

# What is Binary Search?

In simple terms it is just a [[Python Data View#Searching Algorithms| searching algorithm]] that will **find** the required *data* in an **sorted** array.

The **calculation** part works like this:

1. It find the **middle** of the array
	- This is done by finding the **average** of the *length* of the array
2. If the middle value is the one that we are looking for;
	- We then output the **location** / **address** of the value
3. If the middle value is **less** than the search value
	- It will **increase** the *lower bound*
	- Thus, cutting half of the **lower** part of the array
4. If the middle value is **greater** than the search value
	- It will **decrease** the *upper bound*
	- Thus, cutting half of the **upper** part of the array

This means that **binary search** is really *efficient* and *fast*, as it always **cuts** the array in half each time the value is **not** found.

# Some Advantages

- Run time complexity if 0 ( $log N$ )
- Very fast and efficient for large data sets
	- As is cuts the array in half

# Some Disadvantages

- It is error prone
	- *Off-By-One Errors*
		- Occurs when determining the boundary of the next interval
- Caching is poor

> For more advantages and disadvantages; just [Google](https://google.com) them. The thing is that you need to know is:
> - Understand how it works
> - The actually program code

>[!warning]
>The array needs to be **SORTED** for it to work
>Never forget this.

# Binary Search Code - 1D Array

## Template - 1D Array

This is only the [[Functions and Procedures - Python#Example 5 Binary Search| function]], thus is will **not** run on its own.

```python

# Binary Search Function

# We need to pass 2 arguments inside the function

# We need to pass the array - In this case our array is called "array"
# We need to pass our search value - In this case our array is called "user_find"
def binary_search(array, user_find):

    # Another function what will perform the calculations for the binary search
    
    # In this function we need to pass the:
    # array
    # Mininum size of array = 0
    # length of array - 1
    # search value ( user_find )
    return binary_search_calc(array, 0, len(array) - 1, user_find)
  
# Our function "binary_search_calc()" will perform the calculations

# In this function we need to pass some values for;
# array
# Minimum siz of array = 0 --> "lower" 
# length of array - 1 --> "upper"
# search value ( user_find )
def binary_search_calc(array, lower, upper, user_find):

    # Condition to enter loop ( need to learn theory to understand why )
    while lower <= upper:

        # Calculating our mid value
        mid = (lower + upper) // 2

        # If value at index "mid" is equal to search value ( user_find )
        if array[mid] == user_find:

            return mid

        # If value at index "mid" is lower than search value ( user_find )
        elif array[mid] < user_find:

            # lower takes the index to the right of mid
            # Remove the "lower" part of array
            lower = mid + 1

        else:

            # upper takes the index to the left of mid
            # Remove the "upper" part of array
            upper = mid - 1
            
    # If "user_find" is not found
    return -1

```

## Examples ( Non-Recursive )

### Example 1: Complete Code

```python

# Binary Search

print()

# Array with name "array" and values has already been added
array = [786, 23, 0, 25, 8, 17]

# Ask the user to input a value to find
user_find = int(input("Please Enter A Number To Find: "))

# We need to pass 2 arguments inside the function

# We need to pass the array - In this case our array is called "array"
# We need to pass our search value - In this case our array is called "user_find"
def binary_search(array, user_find):

    # Another function what will perform the calculations for the binary search
    
    # In this function we need to pass the;
    # array
    # Mininum size of array = 0
    # length of array - 1
    # search value ( user_find )
    return binary_search_calc(array, 0, len(array) - 1, user_find)

# Our function "binary_search_calc()" will perform the calculation

# In this function we need to pass some values for;
# array
# Minimum size of array = 0 --> "lower"
# length of array - 1 --> "upper"
# search value ( user_find )
def binary_search_calc(array, lower, upper, user_find):

    # Condition to enter loop ( need to learn theory to understand why )
    while lower <= upper:

        # Calculating our mid value
        mid = (lower + upper) //2

        # If value at index "mid" is equal to search value ( user_find )
        if array[mid] == user_find:

            return mid

        # If value at index "mid" is lower than search value ( user_find )
        elif array[mid] < user_find:

            # lower takes the index to the right of mid
            lower = mid + 1

        else:
  
            # upper takes the index to the left of mid
            upper = mid - 1  

    # If search value has not been found
    return -1

# "result" will take the "answer" from the function "binary_search()"
result = binary_search(array, user_find)

print()

# If the result was not equal to False
if result != -1:

    # Outputs this message
    print(str(user_find) + " has been found at " + str(result))

else:

    # If result was equal to True
    # Outputs this message
    print("Not Found")

print()

# Displaying values of array on separate lines
for i in array:

    print(i)

```

# Binary Search Recursive Code - 1D Array

## Template - 1D Array ( RECUSIVE )

This is only the [[Functions and Procedures - Python | function]], thus is will **not** run on its own.

```python

# Recursive Binary Search Function

# We need to pass 2 arguments inside the function

# We need to pass the array - In this case our array is called "array"
# We need to pass our search value - In this case our array is called "user_find"
def binary_search_recursive(array, user_find):

    # Our function "binary_search_recursive_calc()" will perform the calculations
    
    # In this function we need to pass some values for;
    # array
    # Minimum size of array = 0
    # length of array - 1
    # search value ( user_find )
   return binary_search_recursive_calc(array, 0, len(array) -1, user_find)
   
# Our function "binary_search_recursive_calc()" will perform the calculation

# In this function we need to pass some values for;
# array
# Minimum size of array = 0 --> "lower"
# length of array - 1 --> "upper"
# search value ( user_find )
def binary_search_recursive_calc(array, lower, upper, user_find):

   # Checks if lower is not equal to size of array
   if lower > upper:
   
      # If lower > upper ==> values has NOT been found
      return False

   # Calculating our mid value
   mid = (lower + upper) //2

   # If value at index "mid" is equal to search value ( user_find )
   if array[mid] == user_find:

      return mid

   # If value at index "mid" is greater than search value ( user_find )
   elif array[mid] > user_find:

      # Similar to upper = mid - 1 ( Check "normal" binary search )
      return binary_search_recursive_calc(array, lower, mid - 1, user_find)

   else:

      # Similar to lower = mid + 1 ( Check "normal" binary search )
      return binary_search_recursive_calc(array, mid + 1, upper, user_find)


```

## Examples ( Recursive )

### Example 1: Complete Code

```python

# Recursive Binary Search

print()

# Array with name "array" and values has already been added
array = [786, 23, 0, 25, 8, 17]

# Ask the user to input a value to find
user_find = int(input("Please Enter A Number To Find: "))

# We need to pass 2 arguments inside the function
# We need to pass the array - In this case our array is called "array"
# We need to pass our search value - In this case our array is called "user_find"
def binary_search_recursive(array, user_find):

    # Our function "binary_search_recursive_calc()" will perform the calculations
    # In this function we need to pass some values for;
    # array
    # Minimum size of array = 0
    # length of array - 1
    # search value ( user_find )
   return binary_search_recursive_calc(array, 0, len(array) -1, user_find)

# Our function "binary_search_recursive_calc()" will perform the calculation

# In this function we need to pass some values for;
# array
# Minimum size of array = 0 --> "lower"
# length of array - 1 --> "upper"
# search value ( user_find )
def binary_search_recursive_calc(array, lower, upper, user_find):

   # Checks if lower is not equal to size of array
   if lower > upper:
   
      # If lower > upper ==> values has NOT been found
      # If you are going to use the "if result != ..." code
      # We need to return -1 instead of False
      # This is due to reserved words in Python
      return -1

   # Calculating our mid value
   mid = (lower + upper) //2

   # If value at index "mid" is equal to search value ( user_find )
   if array[mid] == user_find:

      return mid

   # If value at index "mid" is greater than search value ( user_find )
   elif array[mid] > user_find:

      # Similar to upper = mid - 1 ( Check "normal" binary search )
      return binary_search_recursive_calc(array, lower, mid -1, user_find)

   else:

      # Similar to lower = mid + 1 ( Check "normal" binary search )
      return binary_search_recursive_calc(array, mid + 1, upper, user_find)

# "result" will take the "answer" from the function "binary_search()"
result = binary_search_recursive(array, user_find)

print()

# If the result was not equal to False
if result != False:

  # Outputs this message
  print(str(user_find) + " has been found at " + str(result))

else:

  # If result was equal to True
  # Outputs this message
  print("Not Found")

print()

# Displaying values of array on separate lines
for i in array:

    print(i)

```

# [[Arrays - Python#Two Dimensional Arrays ( 2D-Arrays ) | Two Dimensional Arrays]]

---

# Socials

- [**Instagram:**](https://www.instagram.com/s.sunhaloo/)
- [**YouTube:**](https://www.youtube.com/@s.sunhaloo539/streams)

---
Thank You!