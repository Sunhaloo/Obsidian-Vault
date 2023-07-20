---
alias: Python Basics
tag: python
date: 02-07-2023
---

---

## List Of Contents:

- [[Python Basics#What is Python? | What is Python?]]
- [[Python Basics#Python Basics | Python Basics]]
	- [[Python Basics#How to use comment in Python | How to use comment in Python]]
- [[Python Basics#How to Display Text, Values, Variables, and more | How to Display Text, Values, Variables, and more]]
	- [[Python Basics#Displaying Text, Numbers and Decimals | Displaying Text, Numbers and Decimals]]
	- [[Python Basics#Constants and Variables | Constants and Variables]]
		- [[Python Basics#How to check if a *variable* or *constant* is of what datatype | How to check if a *variable* or *constant* is of what datatype]]
	- [[Python Basics#Multiple Assignments | Multiple Assignments]]
	- [[Python Basics#Strings | Strings]]
	- [[Python Basics#Integers | Integers]]
	- [[Python Basics#Floating Point Numbers ( Decimal Numbers ) | Floating Point Numbers ( Decimal Numbers )]]

---

# What is [Python](https://en.wikipedia.org/wiki/Python_(programming_language))?

Python is a high-level ( uses english like words ), *general-purpose* programming language.
Its design philosophy **emphasises** *code readability* with the use of significant indentation via the [off-side rule](https://en.wikipedia.org/wiki/Off-side_rule)

# Python Basics

## How to use comment in Python

To write a comment use:

- *"#"* ( hash  ) symbol.

>[!note]
>Remember a comment is not intepreted when running the program code.

```python

#This is a comment in python 
#This can be used to annotate your python codes

```

# How to Display Text, Integers, Decimals, Variables, and more

To display ( *"print"* ) something in python use the "print()" function.

## Displaying Text, Numbers and Decimals

```python

#Displaying Nothing / Display a Blank Line
print()

#Displaying Text
print("Hello People!")
print()
print("This is a line of text.")
print()
print("Bye! Have a good time.")
print()

#Outputs:
#
#Hello People!
#
#This is a line of text.
#
#Bye! Have a good time.

#Displaying Numbers
#A whole number is called an integer number in programming 

#Displaying Integers ( Whole Numbers )
print(1234)
print(34016)
print(3)

#A decimal number is called a floating point number in programming 

#Displaying Floating Point Numbers
print(3.142)
print(12.121234)
print(4571)

#Outputs:
#3.142
#12.121234
#4571

```

## Constants and Variables

A **constant** does *not* change during the execution of a program.
A **variable** *can* change during the execution of a program

```python

#Creating Constants
brand = "Asus" #"brand" is of type String
pi = 3.142 #"pi" is of type Float
num = 55 #"num" is of type Integer

#Remember for Booleans, there is only "True" or "False"
false = True #"false" is of type Boolean
true = False #"true" is of type Boolean

#This will only create the constants and will NOT display the "values"

#To display use the "print()" function

#Displaying Constants
print(brand)
print()
print(pi)
print()
print(num)
print()
print(false)
print()
print(true)

#Outputs:
#Asus
#
#3.142
#
#55
#
#True
#
#False

```

## How to check if a *variable* or *constant* is of what datatype

To check the **datatype** of something, use:

- *"type()"* function

**Format:**

- type(x)
	- Where *"x"* can be a variable / constant / string / integer / float / boolean

```python

#Example:

print(type("Hello People!"))
print(type(55))
print(type(3.142))
print(type(True))
print(type(False))

#Outputs:
#<class 'str'>
#<class 'int'>
#<class 'float'>
#<class 'bool'>
#<class 'bool'>

#Using Constants
#Assigning Constants
hello = "Hello World!"
num = 55
pi = 3.142
boolean_1 = True
boolean_2 = False

#Displaying Constants
print(type(hello))
print(type(num))
print(type(pi))
print(type(boolean_1))
print(type(boolean_2))

#Outputs:
#<class 'str'>
#<class 'int'>
#<class 'float'>
#<class 'bool'>
#<class 'bool'>

```

## Multiple Assignments

### Example:

```python

#Multiple Assignment

x, y, z, pi = "Hello", 55, True, 3.142
#This means that:
#"x" is equal to "Hello"
#"y" is equal to 55
#"z" is equal to True
#"pi" is equal to 3.142

#Or when "variables" / "constants" have the same values
pi = pi_1 = PI = CONST_PI = 3.142
#This means that:
#"pi" is equal to 3.142
#"pi_1" is equal to 3.142
#"PI" is equal to 3.142
#"CONST_PI" is equal to 3.142

```


## Type Cast

Used to convert a datatype to another datatype

### Example:

- When we need to display total of a number 
	- We need to convert total to the string datatype
- When we need to display the height ( float datatype ) of a person 
	- We need to convert height to the string datatype

```python

#Type Cast

name = "George Russell" #Type is String
num = "63" #Type is String
num_1 = 44 #Type is Integer
merc = True #Type is Boolean
speed = 319.0 #Type is Float

#Displaying Values
print("My name is " + name)
print("My number is "+ num)

#To display the boolean value with some text, we need to convert it to string datatype
print("Driving: " + str(merc))

#Outputs:
#My name is George Russell
#My number is 63
#Driving: True

#Performing a addition with numbers and decimals

#Converting "num" to integer datatype by using a variable

int_num = int(num)

total = int_num + num_1 #"total" is of type integer

print("Total = " + str(total))

#Outputs:
#Total = 107

#Addition FLoating Point Numbers directly without using another variable

print("Decimal Addition = " + str(float(total) + speed) + " kmph")
#Remember "total" was of type Integer

#Outputs:
#Decimal Addition: 426.0

#If this code was copied, when run; It will output:

#My name is George Russell
#My number is 63
#Driving: True
#Total = 107
#Decimal Addition = 426.0 kmph

```

## Strings

Any character found on the keyboard like "a", "b", "@", "%"

For **String Manipulation**, please check the *"[[String Manipulations in Python]]"*

>[!warning]
>You **cannot** perform *mathematical calculations* with it

```python

#Assigning Values
first_name = "Lewis"
last_name = "Hamilton"
full_name = first_name + last_name 
full_name1 = first_name + " " + last_name

#NOTE
#The "+" is used to concaternate ( join ) variables/constants

#Displaying Values
print(first_name)
print()
print(last_name)
print()
print(full_name)
print()
print(full_name1)

#Outputs:
#Lewis
#
#Hamilton
#
#LewisHamilton
#
#Lewis Hamilton

```

## Integers

Integer datatypes are **whole numbers**

>[!warning]
>Integer datatypes are not written in between *quotes*

### Example:

```python

#Making a Simple Addition Calculation
num = "55" #Note that num is of type String
num_1 = "44" #Note that num_1 is of type String
num_2 = 63 #Note that num_2 if of type Integer

#Thus to perform addition we need to convert num and num_1 to integer

#There are 2 ways we could do this:

#1st Method: Using Another Variable 

#Use another variable to hold the converted string

int_num = int(num) 
int_num_1 = int(num)

#This means that int_num and int_num_1 will be of type Integer, thus we can perform other addition

total = int_num + int_num_1 + num_2
#Remember that num_2 is already of type Integer

#Displaying Total of the 3 Numbers
print(total)

#Outputs:
#162

#2nd Method: Using int() directly

total = int(num) + int(num_1) + num_2
#Remember that num_2 is already of type Integer

print(total)

#Outputs:
#162

#Now if we would like to print "total" with some text we would need to convert it

#Again
#We could use a variable that will hold the converted integer value
#Or
#We could directly change it to string

#I will be using the second method;

print("The total is " + str(total))

#Outputs:
#The total is 162

#If this code was copied, when run; It will output:

#162
#162
#The total is 162

```

## Floating Point Numbers ( Decimal Numbers )

>[!info]
>Same as [[Python Basics#Integers | Integers]] but need to change all "int()" to "float()"

S.Sunhaloo