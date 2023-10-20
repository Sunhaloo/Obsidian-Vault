---
Alias: Python OOP
Tag: python, basics
Author: S.Sunhaloo
Type: Computer OOP
Date: 2023-10-16
Status: In-Progress
---

## List of Contents

- [[Computer Object Oriented Programming#What is Computer Object Oriented Programming | What is Computer Object Oriented Programming]]
- 

---

# What is Computer Object Oriented Programming

Basically, whenever we think of "*OOP*"; we need to think **objects** ( like real world objects ).

We have:

- Objects: Which means "an entity that exists in the real world"

This is why we have *Computer **Object** Oriented Programming*

## Structure of OOP

- Classes
	- They are **user-defined** data types that acts as *blueprints* for objects, attributes, and methods
- Objects
	- These are **instances** of a class with *specifically* defined data types.
	- When a class is defined initially, the *description* is the **only** object that is defined
- Methods
	- These are **[[Functions and Procedures - Python | functions]]** that are defined **inside** a class that describe the behaviour of an object. They are useful for re-usability or keeping functionality *[[Computer Object Oriented Programming#Encapsulation | encapsulated]]* inside one object at a time.
- Attributes
	- These are *defined* in the **class template** and represent the **state** of an *object*
	- Objects contain data stored in the attribute field

>As you might have guessed, this is not my work; it is from [freeCodeCamp](https://www.freecodecamp.org/news/what-is-object-oriented-programming/)

## Principles of OOP

### Encapsulation:

It is the **binding** of data together. *Functions* **manipulate** the info and keep it safe. **No direct access** is granted to the info in case it is *hidden*.
To be able to access the information; you need to **interact** with the article in charge of that information.

### Abstraction:

It is the use of simple classes to represent complexity. Basically, we use abstraction to **hide** the *complex codes* by allowing the user to only see relevant information.

### Inheritance:

It allows other classes to follow the same *pattern* of other classes.
For Example:

Cars generally have 4 wheels and 4 doors ( excluding boot ); but so do *vans* and $4 \times 4$.

Hence, we could use the same bit of code from *cars*.

### Polymorphism:

This is the power of 2 **different** *objects* to reply to one form. Program will determine which usage is critical for every execution of the thing form the parent class which reduces code duplication.
It also allows different kinds of objects to interact with the same interface.

