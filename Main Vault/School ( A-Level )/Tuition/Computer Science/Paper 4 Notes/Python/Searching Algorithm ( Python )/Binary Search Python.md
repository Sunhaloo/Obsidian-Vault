---
alias: Binary Search Python
tag: python
date: 22-07-2023
---

---

## List Of Contents:

- [[Binary Search Python#What is a [Binary Search](https://en.wikipedia.org/wiki/Binary_search_algorithm)? | What is a Binary Search?]]
- [[Binary Search Python#Advantages of Binary Search: | Advantages of Binary Search]]
- [[Binary Search Python#Disadvantages of Binary Search: | Disadvantages of Binary Search]]
- [[Binary Search Python#Binary Search Code: | Binary Search Code]]
- [[Binary Search Python#Examples: Binary Search| Examples of Binary Search]]
- [[Binary Search Python#Binary Search Recursive Code: | Binary Search Recursive Code]]
- [[Binary Search Python#Examples: Recursive Binary Search| Examples of Recursive Binary Search]]

---

# What is a [Binary Search](https://en.wikipedia.org/wiki/Binary_search_algorithm)?

A **binary search** is also known as *half-interval search*, *logarithmic search*, *binary chop*.

It is a **searching algorithm** that will find the position of an item in a **sorted array**

It does an average calculations with the length of the array and *"cuts"* the array as necessary to find the required items.
If it does not find the item *after* cutting the array in half, it **again** cuts the array in half until item if found or not found

>[!warning]
>The array needs to be **sorted**
>Else it will **not work**

# Advantages of Binary Search:

- Since its **run time complexity is 0** ( *"log N"* )
- Cuts the array in half, very fast for large data items.

# Disadvantages of Binary Search:

- It is error prone
	- Off-by-One Errors; determining the boundary of next interval
- Caching is poor

# Binary Search Code:

## Binary Search Function:

This is the **function** of linear search; it will **not** run on its own.

```python

# Binary Search Function

# We need to pass 2 arguments inside the function
# We need to pass the array - In this case our array is called "array"
# We need to pass our search value - In this case our array is called "user_find"
def binary_search(array, user_find):

    # Another function what will perform the calculations for the binary search
    # In this function we need to pass the;
    # array
    # length of array - 1
    # search value ( user_find )
    return binary_search_calc(array, 0, len(array) - 1, user_find)
  
# Our function "binary_search_calc()" will perform the calculations
# In this function we need to pass some values for;
# array
# length of array - 1
# search value ( user_find )
def binary_search_calc(array, lower, upper, user_find):

    # Condition to enter loop ( need to learn theory to understand why )
    while lower <= upper:

        # Calculating our mid value/average
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
            
    # If not found
    return False

```

# Examples: Binary Search

## Example 1:

This is an example where the array already has values in it.

```python

# Binary Search Function

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
    # length of array - 1
    # search value ( user_find )
    return binary_search_calc(array, 0, len(array) - 1, user_find)

# Our function "binary_search_calc()" will perform the calculations
# In this function we need to pass some values for;
# array
# length of array - 1
# search value ( user_find )
def binary_search_calc(array, lower, upper, user_find):

    # Condition to enter loop ( need to learn theory to understand why )
    while lower <= upper:

        # Calculating our mid value/average
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

    # If not found
    return False

# "result" will take the "answer" from the function "binary_search()"
result = binary_search(array, user_find)

# This code will allow us to use mid in a print() function
mid = binary_search(array, user_find)

print()

# If the result was not equal to False
if result != False:

    # Outputs this message
    print(str(user_find) + " has been found at " + str(mid))

else:

    # If result was equal to True
    # Outputs this message
    print("Not Found")

# Displaying values of array on separate lines
for i in array:

    print(i)

```

# Binary Search Recursive Code:

## Binary Search Recursive Function:

This is the **function** of linear search; it will **not** run on its own.

```python



```

# Examples: Recursive Binary Search

## Example 1:

```python



```
