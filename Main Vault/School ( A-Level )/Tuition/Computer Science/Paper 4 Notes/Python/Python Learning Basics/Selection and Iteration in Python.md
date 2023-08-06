---
alias: Selection and Iteration in Python
tag: python
date: 03-07-2023
---

---

## List Of Contents:

- [[Selection and Iteration in Python#IF Statements| IF Statements]]
- [[Selection and Iteration in Python#WHILE Loops| WHILE Loops]]
- [[Selection and Iteration in Python#FOR Loops| FOR Loops]]
- [[Selection and Iteration in Python#Break, Continue, Pass| Break, Continue, Pass]]
	- [[Selection and Iteration in Python#Break| Break]]
	- [[Selection and Iteration in Python#Continue| Continue]]
	- [[Selection and Iteration in Python#Pass| Pass]]

---

# IF Statements

## Example of If Statements:

### Example 1:

This code below will ask the user to enter his/her age and display a message accordingly

```python

#IF Statements

#Asking the user to input his age

user_age = int(input("Please Enter Your Age: "))

if user_age >= 18 and user_age < 100:

    print("You are an adult!")  

elif user_age <= 0:

    print("Error!")

elif user_age >= 100:

    print("Congratulations! You are about to die")

elif user_age >= 1 and user_age <= 18:

    print("You are a child!")

```

### Example 2:

This code below will ask the user to enter the temperature and display a message accordingly

```python 

#Asking the user to input the temperature
temp = int(input("What is the temparature: "))

if temp >= 0 and temp <= 40:

    print("Normal Temperature!")

elif temp >= 41 and temp <= 100:

    print("Very Hot")

elif temp < 0:

    print("Very Cold")  

else:

    print("Extreme Temperature")

```

---

# WHILE Loops

### Example:

This code below will ask the user to his phone number and display a message accordingly

>[!warning]
>This code will *stop* running **after** the user enters his phone number

```python

tel_num = ""

#or tel_num = None

while len(tel_num) == 0:

#or while not tel_num  

    tel_num = input("Please Enter A Telephone Number: ")

print("Your Telephone Number is " + tel_num)

```

---

# FOR Loops

## Examples of FOR Loops:

### Example 1:

This code below will display numbers from 1 to 10

Format:

- range(x)
	- Where x is an integer number
		- It will display from 0 to x -1

```python

#Display numbers from 1 to 10

for i in range(11):

    print(i)

```

### Example 2:

This code below will display numbers from 20 to 25

Format: 

- range(x, y)
	- Where x and y are integer values
		- It will display from x + 1
		- It will display to y - 1

```python

#Display number from 20 to 25

for j in range(19, 25): #Display number from 20 to 24

    #Displays number from 20 to 25, as j has 1 added to it

    print(j + 1)

```

### Example 3:

This code below will display numbers from 20 to 25

Format: 

- range(x, y, z)
	- Where x, y and z are integer values
		- It will display from x + 1
		- It will display to y - 1
		- It will display in steps of z

```python

#Display numbers from 0 to 10 in steps of 2

for k in range(0, 11, 2):

    print(k)

```

### Example 4:

This code below will ask the user to input his name and it will display his name


```python

#Asking the user to enter his name
name = input("Please Enter Your Name: ")

for x in name:

    print(x, end = "")
    #"end = """ will not move the cursor to the next line

```

### Example 5:

This code below will ask the user the user to input the number of rows, columns and will also ask to input a character that will be used to make a grid

```python 

#Asking the user to input data
rows = int(input("Please Enter Number Of Rows: "))
columns = int(input("Please Enter Number Of Columns "))
symbol = input("Please Enter A Symbol To Use: ")

rows = int(input("Please Enter Number Of Rows: "))

columns = int(input("Please Enter Number Of Columns "))

symbol = input("Please Enter A Symbol To Use: ")

  

print()

  

for v in range(rows):

    for n in range(columns):

        print(symbol, end = "")
        #"end = """ will not move the cursor to the next line

    print()
    #Display the grid

```

---

# Break, Continue, Pass

## Break

It is used to terminate a loop

### Example:

The **while** loop will not stop **until** the user *inputs* his name

```python

while True:

    name10 = input("Please Enter Your Name: ")

    if name10 != "": #!= ==> not equal

        break
        #Exits while loop

```

## Continue

It will skip to the next iteration of the loop

### Example:

```python

mobile_num = "1234-5678"

for o in mobile_num:  

    if o == "-": #Equal ==> "=="

        continue

    print(o, end = "")
    #"end = """ will not move the cursor to the next line

#Outputs:
#12345678

```

## Pass

It **skips** an *"item"*; It acts as a placeholder

### Example:

```python

print()

for p in range(0, 21):
#This displays numbers from 0 to 20

    if p == 13:

        pass
        #This skips number 13

    else:

        print(p)
        #Displays numbers from 0 to 20; and does not display 13

```

---

S.Sunhaloo