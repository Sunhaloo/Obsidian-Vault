---
alias: Math Function in Python
tag: python
date: 03-07-2023
---

---

## List Of Contents:

- [[Math Function in Python#Rounding Numbers| Rounding Numbers]]
- [[Math Function in Python#ABS Function| ABS Function]]
- [[Math Function in Python#Power Function| Power Function]]
- [[Math Function in Python#Max Function| Max Function]]
- [[Math Function in Python#Min Function| Min Function]]
- [[Math Function in Python#Ceil Function| Ceil Function]]
- [[Math Function in Python#Floor Function| Floor Function]]
- [[Math Function in Python#Square Root Function| Square Root Function]]

---

## Rounding Numbers

To round a number use the round() function

Format:

- round("x")
	- Where x is an float/variable/string

```python

#Round

pi = 3.142
num = 55.55
num1 = 55.4545

#rounding numbers

print(round(pi))
print(round(num))
print(round(num1))

#Outputs:
#3
#56
#55

```

>[!note]
>Return data of **float** datatype

## ABS Function

It is used to make a **negative** number become **positive**

Format:

- abs(x)
	- Where x is an integer/float

```python

#ABS

neg_pi = -3.142
neg_num = -55

print(abs(neg_pi))
#This will return data of the float type

print(abs(neg_num))
#This will return data of the integer type

#Outputs:
#3.142
#55

```

## Power Function

It is used to increase a number to the power

Format:

- pow(x, y)
	- Where x is the base ( can be an integer/float )
	- Where y is the power ( can be an integer/float )

```python 

#Power

num= 55
pi = 3.142

#Calculate the value of "num" to the power of 2

print(pow(num, 2))
#This will return data of the integer type

#Outputs:
#3025

#Calculate the value of "pi" to the power of 1.5

print(pow(pi, 1.5))
#This will return data of the float type

#Outputs:
#5.569411036007308

#If this code was copied, when run; It will output: 

#3025
#5.569411036007308

```

## Max Function

It is used to find the **maximum** values between some numbers

Format:

- max(x, y, z)
	- Where x, y and z can be an integer/float

```python

x = 1
y = 2
z = 3

#Display the maximum value of the 3 numbers

print(max(x, y, z))

#Outputs:

#3

```

## Min Function
It is used to find the **minimum** values between some numbers

Format:

- min(x, y, z)
	- Where x, y and z can be an integer/float

```python

x = 1
y = 2
z = 3

#Display the minimum value of the 3 numbers

print(min(x, y, z))

#Outputs:

#1

```

>[!warning]
>The functions below will require the "import maths" module for them to work
>The see all the modules in python; type "help("modules")"

## Ceil Function

It will *round* a number **up** to the nearest integer

Format:

- math.ceil(x)
	- Where x can be an float/integer

```python

#Ceil

#Importing Math Module
import math

pi = 3.142

#Apply ceil to "pi"

print(math.ceil(pi))
#This will return data of the type integer

#Outputs:

#4

```

>[!note]
>When used, it will return data of **integer** datatype

## Floor Function

It will *round* a number **down** to the nearest integer

Format:

- math.floor(x)
	- Where x is an float/integer

```python

#Floor

#Importing Math Module
import math


pi = 3.142

#Apply floor to "pi"

print(math.floor(pi))
#This will return data of the type integer

#Outputs

#3

```

>[!note]
>When used, it will return data of **integer** datatype

## Square Root Function

It will return the **squre root** of any number

Format:

- math.sqrt(x)
	- Where x can be an integer/float

```python

#Square Root

#Importing Math Module
import math

num = 4
pi = 3.142

#Calcuate the square root of "num"

print(math.sqrt(num))

#Outputs:

#2.0

#Calcuate the square root of "pi"

print(math.sqrt(pi))

#Outputs:

#1.7725687574816384

```

>[!note]
>When used, it will return data of **float** datatype

S.Sunhaloo