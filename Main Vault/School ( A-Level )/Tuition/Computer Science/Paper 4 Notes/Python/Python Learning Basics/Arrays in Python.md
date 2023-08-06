---
alias: Arrays in Python
tag: python
date: 03-07-2023
---

---

## List Of Contents:

- [[Arrays in Python#What is an Array?] | What is an Array?]]
- [[Arrays in Python#One Dimensional Array ( 1D-Array ) | One Dimensional Array ( 1D-Array )]]
	- [[Arrays in Python#Example 1: Display | Display]]
	- [[Arrays in Python#Example 2: Display At Specific Location | Display At Specific Location]]
- [[Arrays in Python#Adding an Item at the End of the 1D-Array | Adding an Item at the End of the 1D-Array]]
- [[Arrays in Python#Removing Items from 1D-Array | Removing Items from 1D-Array]]
	- [[Arrays in Python#Removing an Item an the End of the 1D-Array | Removing an Item an the End of the 1D-Array]]
	- [[Arrays in Python#Removing an Item from 1D-Array | Removing an Item from 1D-Array]]
- [[Arrays in Python#Inserting Data in 1D-Array | Inserting Data in 1D-Array]]
	- [[Arrays in Python#Inserting Data at a Specific Address | Inserting Data at a Specific Address]]
- [[Arrays in Python#Clearing a 1D-Array | Clearing a 1D-Array]]
- [[Arrays in Python#Let User Enter Data Into Array | Let User Enter Data Into Array]]
- [[Arrays in Python#Two Dimensional Array ( 2D-Array ) | Two Dimensional Array ( 2D-Array )]]

# What is an Array?

In computer science, an array is a 

- **Data structure** consisiting of a collection of *values* or *variables* of **same** memory size each by at least one array index. 
- Used in places where data need to be:

	1. Entered in a list
	2. Searched
	3. Sorted

- Algorithms that uses array:

	- [[Bubble Sort]]
	- [[Linear Search Python]]
	- [[Binary Search Python]]

- Data Structures that uses array:

	- [[Stack Abstract Data Type ( Python )]]

---

# One Dimensional Array ( 1D-Array )

### Example 1: Display

The code below will display the 2 arrays

```python
#1D-Array

cars = ["Rx-7", "Supra", "AE-86","GT-86", "GTR-R32", "McLaren-P1", "Porsche-918-Spyder", "Koenisegg-Regera-R", "Lancer-MR9"]
numbers = [1, 2, 3, 4, 5]
float_numbers = [1.2, 2.3, 3.4, 4.5, 5.6]

#Displaying Arrays

print()
print("Displaying Arrays")
print()

print(cars)
print(numbers)
print(float_numbers)

print()
print("Displaying Arrays (each item on different lines) ")
print()  

#Another way to display ( Displays on another line each time )

for x in cars:

    print(x)

print()  

for y in numbers:

    print(y)

print()

for z in float_numbers:

    print(z)

```
>[!note]
>Arrays are of datatype **list**

### Example 2: Display At Specific Location

The code below will display elements of the arrays at a specific adrress

```python

#1D-Array

cars = ["Rx-7", "Supra", "AE-86","GT-86", "GTR-R32", "McLaren-P1", "Porsche-918-Spyder", "Koenisegg-Regera-R", "Lancer-MR9"]

#Displaying Elements At Specific Address:
print("Car 1: " + cars[0])
print("Car 3: " + cars[2])
print("Car 7: " + cars[6])
print("Car 8: " + cars[7])

```

## Adding an Item at the End of the 1D-Array

Format:

- x.append()
	- Where x is an array/list

```python

#Adding Data To 1D-Array

food = ["pizza", "sushi", "briani", "oreos"]

print(food)

#Add "ice-cream" to the array

food.append("ice-cream")

#Displays New Array
print(food)

```

## Removing Items from 1D-Array

### Removing an Item an the End of the 1D-Array

Format:

- x.remove()
	- Where x is an array/list

```python

#Removing Last Data From 1D-Array

food = ["pizza", "sushi", "briani", "oreos"]

print(food)

#Add "ice-cream" to the array

food.pop()

#Displays New Array
print(food)

```

### Removing an Item from 1D-Array

Format:

- x.remove(y)
	- Where x is an array/list
	- Where y can be a string/integer/float

```python

#Removing Data From 1D-Array

food = ["pizza", "sushi", "briani", "oreos"]

print(food)

#Remove "oreos" to the array

food.remove("oreos")

#Displays New Array
print(food)

```

## Inserting Data in 1D-Array

### Inserting Data at a Specific Address

Format:

- x.insert(y, z)
	- Where x is an array/list
	- Where y is the adrress
	- Where z is the data to insert ( can be string, integer, float )

```python

#Adding Data to 1D-Array At Specific Location

food = ["pizza", "sushi", "briani", "oreos"]

print(food)

#Remove "cake" to the array

food.insert(0,"cake")

#Displays New Array
print(food)

```

## Clearing a 1D-Array

It will remove everying from the array

Format:

- x.clear()
	- Where x is an array/list

```python

#Clearing Data From 1D-Array

food = ["pizza", "sushi", "briani", "oreos"]

print(food)

#Remove "cake" to the array

food.clear()

#Displays New Array
print(food)

```

## Let User Enter Data Into Array

### Code:

```python

#1D-Arrays

#These are the 1D-Arrays
name = [] #"name" will be of size 5 and will data of the string datatype
numbers = [] #"numbers" will be of size 3 and will data of the integer datatype

#"x" is our counter for "name" array
for x in range(5):

    user_name = input("Please Enter A Name: ") #Ask the user to enter data
    name.append(user_name) #Adds data entered by user to array
    
print()

try: #This is exception handling in Python

    #"x" is our counter for "name" array
    for y in range(3):

        user_num = int(input("Please Enter A Number: ")) #Ask the user to enter data
        numbers.append(user_num) #Adds data entered by user to array

except ValueError: #If user enters a character, it will display this message

    print()
    print("Only Enter Numbers!")

print()

#Display Each Array

#Displaying "name" array

print("Names Array:")

for x in name:  

    print(x)

print()

#Displaying "numbers" array

print("Numbers Array:")

for y in numbers:

    print(y)

print()

```

---

# Two Dimensional Array ( 2D-Array )

*2D-Arrays* are made from **1D-Arrays**

## Example:

```python

#1D-Arrays
drinks = ["coffee", "tea", "soda"]
dinner = ["pizza", "hamburger", "hotdog"]
dessert = ["cake", "ice cream"]

#"food1" is a 2D-Array
food1 = [drinks, dinner, dessert]

#Displaying Array
print(food1)

#Another way to display ( Displays on another line each time )

print()
print("Displaying Arrays (each item on different lines) ")
print()

for x in food1:

    print(x)

```

## Array With Specific Size

## Examples:

### Example 1: User enters the size of the array himself

```python

#User Enter Size Of Array

#Array with identifier name: Array_1
#Array_1 has infinite size
#Let "Array_1" be of data type "String"
Array_1 = []

#Asking the user to enter size of array
user_length_array = int(input("Please Enter The Size Of The Array: "))

#Displaying Array
#When displayed, Array_1 will not show any sign that it has a size
print("Displaying Array ( EMPTY )")
print(Array_1)

#To check its size:
#We can ask the user to enter values into the array

#Asking the user to enter data into array
for x in range(user_length_array):

    #Ask the user to input data
    user_string = input("Enter Something: ")
    #Appending data From user to Array
    Array_1.append(user_string)

#Display Array after Input
print(Array_1)

```


### Example 2: With 2 Arrays

```python

#Declare Global Array
#NOTE: This is also "infinite" but it shows the examinor that it has a size
Array_None = []

#Displaying Array
#NOTE: This is also "infinite" but it shows the examinor that it has a size
print()
print("Array_None: " + str(Array_None))

#Declare Global Array
Array_0 = []

#Displaying Array
print()
print("Array_0: " + str(Array_0))
print()

#We can ask the user to enter values into the array

#For Array_None
#DECLARE Array_None: Array[0:4] OF STRING

#Asking the user to input data of "String" data-type

#If we do "for x in Array_None"; It would have been INFINITE
for x in range(5):

    #Asking the user to input a Name
    #Note that "user_name" is of type "String"
    user_name = input("Please Enter A Name: ")

    #Checking if data input by user is a "String"
    if user_name.isdigit():

        #Outputs: "Please Enter Alphabet Only!" if user enters a number
        print()
        print("Please Enter Alphabets Only!")
        print()
        #Exits Program
        break

    else:

        #If user inputs data of type "String"
        user_name = str(user_name) #This line was not necessary
        #It will "append" data into array
        Array_None.append(user_name)

#Displaying Array_None:
print()
print("Array_None:")

#Displaying array in a list
for i in Array_None:

    print(i)

#For Array_0
#DECLARE Array_0: Array[0:1] OF INTEGER

#Asking the user to input data of "Integer" data-type
print()

#If we do "for x in Array_None"; It would have been INFINITE
for y in range(2):

    #Exception Handling
    try:

        #Ask the user to input a Number
        #Note that "user_value" is of type "Integer"
        user_value = int(input("Please Enter A Number: "))
        Array_0.append(user_value)

    except ValueError:

        print()
        print("Please Enter Numbers Only!")
        print()
        break

#Displaying Array_0:
print()
print("Array_0:")

#Displaying array in a list
for j in Array_0:

    print(j)

print()

```

S.Suhaloo