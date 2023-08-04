---
alias: Stack Abstract Data Type ( Python )
tag: python
date: 04-08-2023
---

---

# List Of Contents

- [[Stack Abstract Data Type ( Python )#What is a [Stack](https //en.wikipedia.org/wiki/Stack_(abstract_data_type) ~ text=In%20computer%20science%2C%20a%20stack,that%20was%20not%20yet%20removed.)? | What is a Stack?]]
- [[Stack Abstract Data Type ( Python )#Stack Program Code | Stack Program Code]]
	- [[Stack Abstract Data Type ( Python )#Implementing Array for Stack | Implementing Array for Stack]]
	- [[Stack Abstract Data Type ( Python )#Display Array | Display Array]]
	- 

---

# What is a [Stack](https://en.wikipedia.org/wiki/Stack_(abstract_data_type)#:~:text=In%20computer%20science%2C%20a%20stack,that%20was%20not%20yet%20removed.)?

It is an [[Abstract Data Types ( Python ) | abstract data type]] that serves as a collection of elements with 2 main **operations**:

- PUSH:
	- To **add** or **insert** an item into the stack/array
- POP:
	- To **remove** or **delete** an item into the stack/array

To understand **stack data structure**; we need to think of it as a *stack of plates*. Picture a stack of plate in your head, try to think that the *plate is a data item*

Now, if we would like to **add**/**insert** a plate into the *stack*; a sane person would *place*/*add* the new plate on top

- This is how the **PUSH** operation works, it adds new items in to the stack/array *at* the **top**

Now, if we would like to **remove**/**delete**, a plate from the *stack*; a sane person would *remove* a plate from the top

- This is how the **POP** operation works, it removes the **last** item *from* the **top**

# Stack Program Code

To implement a stack, we will need to use an [[Arrays in Python | array]] and for this program code I will break it down its [[Functions | functions]]

## Implementing Array for Stack

```python

# Stack Program Code

# Array with identifier name "array" and size = undefined
array = []

```

## Display Array 

This is a function that will be used to display the data values on each line.

```python

# Stack Program Code

# Function with identifier name "display_array"
def display_array():

    # For Loop to circle through array
    for x in array:

        # Display each data items on separate lines
        print(x)

```

## Insert Values

This is a function what will be used to allow a user to enter data into the stack/array.

