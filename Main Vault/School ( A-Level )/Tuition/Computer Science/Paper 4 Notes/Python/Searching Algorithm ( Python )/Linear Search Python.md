---
alias: Linar Search Python
tag: python
date: 19-07-2023
---

---

## List Of Contents: 

- [[Linear Search Python#[Linear Search](https://en.wikipedia.org/wiki/Linear_search)| Linear Search Introduction]]
- [[Linear Search Python#Advantages of Linear Search: | Advantages of Linear Search]]
- [[Linear Search Python#Disadvantages of Linear Search: | Disadvantages of Linear Search]]
- [[Linear Search Python#Linear Search Code: | Code For Linear Search]]
- [[Linear Search Python#Linear Search Function ( With "For Loop" )| Linear Search Function (With "For Loop")]]
- [[Linear Search Python#Example Codes | Example Codes]]
	- [[Linear Search Python#Example 1: With "For Loop" | Example 1]]

---

# [Linear Search](https://en.wikipedia.org/wiki/Linear_search)

A **linear search** which is also known as a sequential search is a method for finding an element within an *array*

It has a *counter* which will repeatedly step into the **array** until the desired data is found. Then it can return the index of the data or return an appropriate message.

## Advantages of Linear Search:

1. It is very easy to implement into the code
2. It is fast with small to medium size arrays ( espcially with today's powerful computers )
3. The array does not need to be sorted
4. It is not affected; when data is added or removed from array

# Disadvantages of Linear Search:

1. It is slow for array that has many data inside as it steps into the array and compares the data one by one

---

# Linear Search Code:

## Linear Search Function ( With "For Loop" )

This is the **function** of linear search; it will **not** run on its own.

```python

# Linear Search Function

# Function with identifier name "linear_search"
# 2 "Arguments" need to be passed in function
# These arguments are: 1. Array and 2. Variable that hold the value to be searched
def linear_search(array, value_to_be_searched):

	# Stepping into array ( from 0 to end/length of array )
	for i in range(0, len(array)):

		# Checks if value at index is equal to value to be searched
		if array[i] == value_to_be_searched:

			# If value has been found, then it will return the address of the data/value
			return i

	# If value has NOT been found, it will return "-1"
	return -1 
	
```

### Alternative

We could also write it like:

```python

# Linear Search Function

# Function with identifier name "linear_search"
# 2 "Arguments" need to be passed in function
# These arguments are: 1. Array and 2. Variable that hold the value to be searched
def linear_search(array, value_to_be_searched):

	# Variable "length_array" will keep track of the size of the array
	length_array = len(array)
	# Stepping into array ( from 0 to end/length of array )
	for i in range(0, length_array):

		if array[i] == value_to_be_searched:

			# If value has been found, then it will return "True"
			return True 

	# If value has NOT been found, it will return "False"
	return False
	
```

---

# Example Codes

## Example 1: With "For Loop"

```python

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

except ValueError:

    # If user enters any characters other than integer numbers
    print("Please Enter Whole Number Only!")
    
#Asking the user to add integer data to the array
for x in range(array_size):

    # Variable "user_input" will hold the number entered by the user
    user_input = input("Please Enter A Number: ")

		# Check if user_input is a digit
    if user_input.isdigit():

				# If "user_input" is a digit; convert it into an "Integer" value
        user_input = int(user_input)

    else:

				# If "user_input" is NOT a digit, it will ouput this message
        print("Please Enter Whole Numbers Only!")

    # Adding user data (user input) to the array
    numbers.append(user_input)

# Variable "user_find" will hold the the number to find in the array
print()
user_find = input("Please Enter A Number To Find: ")
print()

# Checking if user input (user_find) is a number
if user_find.isdigit():

    # If user input (user_find) is a number; it converts the user input into an integer data
    user_find = int(user_find)    
    # If user input (user_find) was not a number

else:

    # Then output the following message
    print("Please Enter Whole Numbers Only!")

# Linear Search Function:
def linear_search(numbers, user_find):

    #"For Loop" what will iterates through the array (numbers)
    # It will iterates from 0 to length of the array (numbers)
    for i in range(0, len(numbers)):

        # If value at that index is equal to user input (user_find) then
        if numbers[i] == user_find:

            # Return the index of the search value (user_find)
            return i

    # If value has not been found, then returns "-1"
    return -1

# Calling Function
search_value = linear_search(numbers, user_find)

# Displaying search_value

print(search_value)

```

---
S.Sunhaloo