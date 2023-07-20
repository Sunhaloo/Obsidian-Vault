---
alias: String Methods in Python
tag: python
date: 02-07-2023
---

---

## List Of Contents:

- [[String Manipulations in Python#What is String Manipulations?| What is String Manipulations?]]
- [[String Manipulations in Python#Length Function| Length Function]]
- [[String Manipulations in Python#Find Function| Find Function]]
- [[String Manipulations in Python#Capitalize Function| Capitalize Function]]
- [[String Manipulations in Python#Upper Function| Upper Function]]

---

# What is String Manipulations?

WIth the use of *built-in function*; we can, for example:

- Capitalise first alphabet of a string, or the whole string
- "Uncapitalise" a whole string
- Find the length of a string
- Replace an alphabet with another one in a string
- Find how many "character" are there is a string
- And more!

## Length Function 

It is used to find the length of a string;

Format: 

- len(x)
	- Where "x" is a string/variable/constant

>[!note]
>" " ( space ) is also a character
>Also, len() will **not** start with **0** ( will count characters normally )

### Example:

```python

#Length Function
name = "Toto Woolff"

#If we use the len() function on it is should output: 11

print(len(name))

#Or we could have passed the name directly

print(len("Toto Woolff"))

#Outputs
#11
#11

```

## Find Function

It is used to find the **address** of a specific character

Format: 

- x.find("y")
	- Where "x" is a string/variable/constant
	- Where "y" is the character to find

It will return the **address** of the character

>[!note]
>" " ( space ) is also a character
>Will return an *integer* value
>Also, .find() **will** start with **0** ( will count characters normally )

```python

#Finding the position of a character in a string
name = "W11" 

#Example: Find "W"

#There are 2 methods we could take:

#1st Method: Using Another Variable

find_name = name.find("W")

print(find_name)

#Outputs:
#0

#2nd Method: Using .find() directly

print(name.find("W"))

#Outputs
#0

#If this code was copied, when run; It will output:

#0
#0

```

## Capitalize Function

It is used to *capitalize* the **first** character of a string

Format:

- x.capitalize()
	-  Where "x" is a string/variable/constant

```python

#Capitalize

#There are 2 Methods that we can use to Capitalise a String

#1st Method: Using Another Variable

name = "charles Leclerc"

fcap_name = name.capitalize()
#This is of the string datatype

print(fcap_name)

#Outputs:
#Charles Leclerc

#2nd Method: Using .capitalize()  directly

print(name.capitalize())
#This is of the string datatype

#Outputs:
#Charles Leclerc

#If this code was copied, when run; It will output:

#Charles Leclerc
#Charles Leclerc

```

>[!note]
>When used, it will return data of **string** datatype

## Upper Function

It is used to *capitalize* the **whole** string

Format:

- x.upper()
	- Where x is a string/variable/constant

```python

#Upper

#There are 2 Methods that we can use to "upper" a String

#1st Method: Using Another Variable

name = "carlos sainz"

cap_name = name.upper()
#This is of the string datatype

print(cap_name)

#Outputs:
#CARLOS SAINZ

#2nd Method: Using .upper()  directly

print(name.upper())
#This is of the string datatype

#Outputs:
#CARLOS SAINZ

#If this code was copied, when run; It will output:

#CARLOS SAINZ
#CARLOS SAINZ

```

>[!note]
>When used, it will return data of **string** datatype

## Lower Function

It is used to *"un-capitalize"* a **whole** string

Format:

- x.lower()
	- Where x is a string/variable/constant

```python

#Lower

#There are 2 Methods that we can use to "lower" a String

#1st Method: Using Another Variable

name = "NICHOLAS LATIFI"

cap_name = name.lower()
#This is of the string datatype

print(cap_name)

#Outputs:
#CARLOS SAINZ

#2nd Method: Using .lower()  directly

print(name.lower())
#This is of the string datatype

#Outputs:
#CARLOS SAINZ

#If this code was copied, when run; It will output:

#nicholas latifi
#nicholas latifi

```

>[!note]
>When used, it will return data of **string** datatype

## Digit Function

It is used to check if a string contains **numbers** or not.

Format:

- x.isdigit()
	- Where x is a string/variable/constant

```python

#Digit

is_num = "1234"
isnot_num = "Not A Number"

print(is_num)
print(isnot_num)

#Outputs:
#1234
#Not A Number

#Checking if they are a number or a string

#There are 2 Methods that we can check is a string is a digit or not a digit

#1st Method: Using Another Variable

check1 = is_num.isdigit()
check2 = isnot_num.isdigit()

print(check1)
print(check2)

#Outputs:
#True
#False

#2nd Methods: Using .isdigit() directly

print(is_num.isdigit())
print(isnot_num.isdigit())

#Outputs:
#True
#False

#If this code was copied, when run; It will output:

#1234
#Not A Number
#True
#False
#True 
#False

```

>[!note]
>When used, it will return data of **boolean** datatype

## Alpha Function

It is used to check if a string is **"alphabetical"** or not

Format:

- x.isalpha()
	- Where x is a string/variable/constant

```python

#Alpha 

is_num = "1234"
isnot_alpha = "James Vowles" #Because of the " " ( space )
isnot_alpha1 = "Otmar.Szafnauer" #Because of the "." ( period )
is_alpha = "FrédéricVasseur"

print(is_num)
print(isnot_alpha)
print(isnot_alpha1)
print(is_alpha)

#Outputs:
#1234
#James Vowles
#Otmar.Szafnauer
#FrédéricVasseur

#Checking if they are a alphabet or not

#There are 2 Methods that we can check is a string is a digit or not a digit

#1st Method: Using Another Variable

check1 = is_num.isalpha()
check2 = isnot_alpha.isalpha()
check3 = isnot_alpha1.isalpha()
check4 = is_alpha.isalpha()

print(check1)
print(check2)
print(check3)
print(check4)

#Outputs:
#False
#False
#False
#True

#2nd Methods: Using .isdigit() directly

print(is_num.isalpha())
print(isnot_alpha.isalpha())
print(isnot_alpha1.isalpha())
print(is_alpha.isalpha())

#Outputs:
#False
#False
#False
#True

#If this code was copied, when run; It will output:

#1234
#James Vowles
#Otmar.Szafnauer
#FrédéricVasseu
#False
#False
#False
#True
#False
#False
#False
#True

```

>[!note]
>When used, it will return data of **boolean** datatype

## Count Function

It is used to **count** how many character ( user input ) are there is a string

Format:

- x.count("y")
	- Where x is a string/variable/constant
	- Where y is the character that will be counted

```python

#Count

name = "Nyck de Vries"

#Counting how many times "e"

print(name.count("e"))

#Outputs:
#2

```

>[!note]
>When used, it will return data of **integer** datatype

## Replace Function

It is used to *replace* **a** character in a string with **another** character

Format:

- x.replace("y", "z")
	- Where x is a string/variable/constant
	- Where y is the character to be replaced
	- Where z is the character that will be replaced

```python

#Replace

text = "Hell0 W0rld"

#Replace "0" with "o"

print(text.replace("0", "o"))

#Outputs:
#Hello World

```

>[!warning]
>It will replace **all** the *"y"* in the string

## Input Function

When we need to ask the user to input something into the program 

Format:

- input("x")
	- Where x is a string

```python

#Input

#Write A program what will ask the user to input 2 numbers
#The program will then add those 2 numbers

num1 = input("Please Enter A Number: ")
num2 = input("Please Enter Another Number")

total = int(num1) + int(num2)
#"total" is to type integer

print("Total: " + str(total))

#Outputs:
#Total: "y"
#Where "y" is the total of the 2 numbers

```

>>[!note]
>When used, it will return data of **string** datatype

S.Sunhaloo