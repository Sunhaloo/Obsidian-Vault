---
alias: Functions
tag: python
date: 03-07-2023
---

---

## Examples Of Functions:

### Example 1: Creating And Calling Functions

```python

#def "function name"(parameter):

def hello(name):

    #Codes Inside Function
    print("Hello " + name)
    print("Have a nice day!")

print()
print("Calling Function")

user_name = input("Please Enter A Name: ")

print()

#Calling function
hello("S.Sunhaloo")

print()

#Calling function
hello("Mate")

print()

#Calling function
#Another way of passing paremeters
hello(user_name)

print()

```

### Example 2: Return Statement

```python

#Return Statement

def multiply(number1, number2):

    result = number1 * number2
    return result

#Another way of passing parameters
d = multiply(3, 3)

#Calling and Displaying Function
print(multiply(5, 5))
print(d)

print()

```

S.Sunhaloo