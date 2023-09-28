---
Alias: Python String Manipualation
Tag: python, basics
Author: S.Sunhaloo
Type: String Manipulation
Date: 18-09-2023
Status: In-Progress
---

# List of Contents

- [[String Manipulation - Python#String Manipulation | String Manipulation]]
	- [[String Manipulation - Python#Length Function | Length Function]]
		- [[String Manipulation - Python#Example Just Finding the Length of things | Example of Length Function]]
	- [[String Manipulation - Python#Find Function | Find Function]]

---

# String Manipulation

To be honest, these are those thing that need be shown how it works first, then that bulbs lights up in your tiny brain :)

Sooo... Lets Start my *Bruddas*!

## Length Function

First up on our list is the mighty length function. There are many use cases where one might need ( "*must*" ) use the **length** function.

>[!tip] Usage
>```python
>len(x)
>```
>Where "*x*" could be:
>- String
>- Constant
>- Array

>[!warning]
>" " ( **space** ) is also a *character*; Thus the function will count "*space*"

### Example: Just Finding the Length of things

I might be combining multiple examples in *one example*

```python

# Length Function

print()

# String Data Types

# DECLARE name: OF STRING
name = "Toto Woolff"

# Outputs the length of "name"
print("Length of Toto Woolff: " + str(len(name)))
print()

# DECLARE name_2: OF STRING
name_2 = "Lewis Hamilton"

# DECLARE name_2_length: OF INTEGER
name_2_length = len(name_2)

# Outputs the length of "name_2"
print("Length of Lewis Hamilton: " + str(name_2_length))
print()

# Arrays

# DECLARE array: OF ARRAY[0:4] OF INTEGER
array = [1, 2, 3, 4, 5]

# Outputs the length of "array"
print("Length of array: " + str(len(array)))
print()

# Integer Numbers

# DECLARE number: OF INTEGER
number = 1234

# Output the length of number
print("Length of number:  " + str(len(str(number))))
print()

```

>[!note]
>Look at "*Integer Numbers*"
>The "*len()*" function will find the *length* of **integer numbers**
>Thus, we need to convert the **constant** *number* to *string*
>Then when we *print*, we need to convert the *len()* function to **string** as the data type of *len()* is **integer**
>Hence,
>```python
>str(len(str(number)))
>```

## Find Function