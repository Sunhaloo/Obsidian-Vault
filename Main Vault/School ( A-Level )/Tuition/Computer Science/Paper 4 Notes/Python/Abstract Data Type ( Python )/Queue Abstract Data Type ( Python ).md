---
Alias: Queue Python
Tag: python
Date: 20-08-2023
---

---

## List Of Contents:

- [[Queue Abstract Data Type ( Python )#What is a [Queue](https //en.wikipedia.org/wiki/Queue_(abstract_data_type))? | What is a Queue]]
- [[Queue Abstract Data Type ( Python )#Queue Program Code | Queue Program Code]]
	- [[Queue Abstract Data Type ( Python )#Insert Data Into Array | Insert Data Into Array]]
		- [[Queue Abstract Data Type ( Python )#Method 1 | First Method]]
		- [[Queue Abstract Data Type ( Python )#Method 2 | Second Method]]
	- [[Queue Abstract Data Type ( Python )#Removing Data From Array | Removing Data From Array]]
		- [[Queue Abstract Data Type ( Python )#Method 1 need to be used with Queue Abstract Data Type ( Python ) Method 1 First Insert Method | First Method]]
		- [[Queue Abstract Data Type ( Python )#Method 2 need to be used with Queue Abstract Data Type ( Python ) Method 2 Second Insert Method | Second Method]]

---

# What is a [Queue](https://en.wikipedia.org/wiki/Queue_(abstract_data_type))?

In [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"), a **queue** is a [collection](https://en.wikipedia.org/wiki/Collection_(abstract_data_type) "Collection (abstract data type)") of entities that are maintained in a sequence and can be modified by the addition of entities at one end of the sequence and the removal of entities from the other end of the sequence. By convention, the end of the sequence at which elements are added is called the back, tail, or rear of the queue, and the end at which elements are removed is called the head or front of the queue, analogously to the words used when people line up to wait for goods or services.

# Queue Program Code

## Insert Data Into Array

### Method 1:

Append data into array using ".append()" function

```python

# Queue Program Code

def insert_item_append(array):

    # Exception Handling
    try:

        # Ask user to enter size of array
        array_size = int(input("Please Enter Size Of Array: "))

        print()

        # Ask user to enter data with respect to size of array
        for x in range(array_size):

            # Ask the user to enter values into array
            user_input = int(input("Please Enter A Value:"))
            array.append(user_input)

    except ValueError:
    
        # Outputs appropriate message
        print("Please Enter Integer Numbers Only")

```

### Method 2:

Insert data into array using ".insert(0, value)" function

```python

# Queue Program Code

def insert_item_append(array):

    # Exception Handling
    try:

        # Ask user to enter size of array
        array_size = int(input("Please Enter Size Of Array: "))

        print()

        # Ask user to enter data with respect to size of array
        for x in range(array_size):

            # Ask the user to enter values into array
            user_input = int(input("Please Enter A Value:"))
            # Inserts at index "0"
            array.insert(0, user_input)

    except ValueError:
    
        # Outputs appropriate message
        print("Please Enter Integer Numbers Only")

```

>[!note]
>Using this method will means that the last item that has been entered will be at index 0
>In short the array will be **reversed** ( in the order of input )

## Removing Data From Array

There are to methods; each work with their own respective **insert**

### Method 1 need to be used with [[Queue Abstract Data Type ( Python )#Method 1 | First Insert Method]]

```python

# Queue Program Code

def remove_pop_WAppend(array):

    # Removing One Item
    print("Removing data at Index '0'")
    array.pop(0)

```

### Method 2 need to be used with [[Queue Abstract Data Type ( Python )#Method 2 | Second Insert Method]]

```python

# Queue Program Code

def remove_pop_WInsert(array):

    # Removing One Item
    print("Removing data at Index '0'")
    array.pop()

```

>[!note]
>Because the array is already "**reversed**"
>There is no need to "*pop*" at index "0"
>Thus we only need to remove the last data value