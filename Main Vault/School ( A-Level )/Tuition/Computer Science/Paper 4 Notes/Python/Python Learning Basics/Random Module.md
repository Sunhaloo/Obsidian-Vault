---
alias: Random Module
tag: python
date: 03-07-2023
---

---

## List Of Contents:

- 

---

# What is the Random Module used for?

It is used to generate random numbers, shuffle data in an array or even display an element randomly from an array

>[!warning]
>To use the random module; we need to type *"import random"* at the start of the code

## Display Random Number 

### Display Random Number in between 0 and 1:

If you want to get a random number between 0 and 1;

Format:

- random.random()
	- It will display a random number between 0 and 1\
	- 

```python

#Random

#Display a random number between 0 and 1 five times

#Import Random Module
import random

print()
print("Displaying Random Numbers")
print()

for x in range(5):

    print("Random Number " + str(x) + " : " + str(random.random()))
    
print()

```

>[!note]
>When used, it will return data of **float** datatype

### Display random number in between any number

Format:

- random.randint(x, y)
	- Where x represent the start and of datatype integer
	- Where y represent the end and of datatype integer

```python

#Random

#Display a random number between 1 and 100 five times

#Import Random Module
import random

print()
print("Displaying Random Numbers")
print()

for x in range(5):

    print("Random Number " + str(x) + " : " + str(random.randint(1, 100)))

print()

```

### Display a Random Item from an Array

Format:

- random.choice(x)
	- Where x is an array/list

```python

#Random

#Rock, Paper, Scissors

#Import Random Module
import random

#1D-Array
list = ['rock', 'paper', 'scissors']
  
#Displaying A Random Item From Array

print(random.choice(list))

```

### Shuffling An Array

Format:

- random.shuffle(x)
	- Where x is an array/list

```python

#Random

#Example From Cards

#Import Random Module
import random

cards = [1, 2, 3, 4, 5, 6, 7, 8, 9, "J", "K", "A"]

random.shuffle(cards) #This line should be like this

#Displaying Shuffled Cards
print(cards)

```

S.Sunhaloo