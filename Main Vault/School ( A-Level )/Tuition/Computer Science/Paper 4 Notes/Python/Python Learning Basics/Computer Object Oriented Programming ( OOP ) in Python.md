---
alias: Computer Object Oriented Programming ( OOP ) in Python
tag: python
date: 03-07-2023
---

---

## List Of Contents:

- [[Computer Object Oriented Programming ( OOP ) in Python#Writing Directly in the Same File| Writing Directly in the Same File]]
- [[Computer Object Oriented Programming ( OOP ) in Python#Writing in Separate Files | Writing in Separate Files]]
- [[Computer Object Oriented Programming ( OOP ) in Python#Inheritance | Inheritance]]
- [[Computer Object Oriented Programming ( OOP ) in Python#Multilevel Inheritance | Multilevel Inheritance]]

---

# Computer Object Oriented Programming ( OOP )

There are 2 ways to make it;

## Writing Directly in the Same File

```python

class Animal:

    #Attributes
    alive = True

    #Methods
    def eat(self):

        print("This animal is eating")

    def sleep(self):

        print("This animal is sleeping")
        
    def running(self):

        print("This animal is running")


#Creating Objects
Cat = Animal()
Dog = Animal()
Gold_Fish = Animal()

#Assigning Values
print(Cat.alive)
print(Dog.alive)
print(Gold_Fish.alive)

#Adding Methods
print("For Cat:")

Cat.running()

print()

print("For Dogs:")

Dog.sleep()

print()

print("For Gold Fish:")

Gold_Fish.eat()

print()

```

## Writing in Separate Files

### File 1: main.py

```python

#Importing From 2nd File
from car import Car
from car import Moto
#from "file name" import "object"

#Making Object
car_1 = Car("Mazda", "RX-7", 1998, "Yellow")
car_2 = Car("Toyota", "Ae86", 1998, "White")
moto_1 = Moto("Kawasaki", "H2", 2015, "Green Carbon Fibre")
  
#NOTE
#"self" is automatically passed

#This will output every detail about car_1

print()

print(car_1.make)
print(car_1.model)
print(car_1.year)
print(car_1.color) 

print()

#This will output every detail about car_2
print(car_2.make)
print(car_2.model)
print(car_2.year)
print(car_2.color)

print()

print(moto_1.make)
print(moto_1.model)
print(moto_1.year)
print(moto_1.colour)

print()

#Calling Methods/Functions
print("Calling Methods:")

print()

print("Driving And Stopping:")
car_1.drive()
car_1.stop() 

print()

print("Driving And Stopping:")
car_2.drive()
car_2.stop()

print()

#Displaying a specific data
print("About Car 1:")

car_1.age()
car_1.paint()

print()  

print("About Car 2:")

car_2.age()
car_2.paint()

print()

print("About Motocycle:")

moto_1.moto() 

print()

#Class Variable

#Display the number of wheels

#If we use
#Car.wheels = 6

#Then all the cars will have 6 wheels

Car.wheels = 6

print("Display The Number Of Wheels:")  

print()

print("Number Of Wheels For Car 1: " + str(car_1.wheels)) 

print() 

print("Number Of Wheels For Car 2: ", end = "")
print(car_2.wheels)

print()

moto_1.wheels = 2

print("Number of Wheel For Moto 1: " + str(moto_1.wheels)) #Wheels have been assigned none in car.py

print()

```

>[!note]
>This is the file that need to be run

### File 2: car.py

```python

class Car:

    #Class Variable
    wheels = 4

    #Constructor
    #def__init__(self):
    def __init__(self, make, model, year, color):

        #Attributes
        #(these are known as instance variables)
        self.make = make
        self.model = model
        self.year = year
        self.color = color

    #Methods
    def drive(self):

        print("This " + self.model + " is driving")

    def stop(self):

        print("This " + self.model + " is stopped")

    def paint(self):

        print("This " + self.model + " is: " + self.color)

    def age(self):

        print(self.model + " Manufactured on: " + str(self.year))

class Moto:

    #Class Variable
    wheels = None
    #Change the values in car.py

    #Constructor
    def __init__(self, make, model, year, colour):
        self.make = make
        self.model = model
        self.year = year
        self.colour = colour
        
    def moto(self):

        print(self.make + " is a motocycle!")

```

>[!info]
>This file is exported to **main.py**

---

## Inheritance

It means to receive, derive, or to be left with

```python

#Inheritance

#Parent Class
class Animal:

    #Attributes
    alive = True

    #Methods
    def eat(self):
    
        print("This animal is eating")

    def sleep(self):

        print("This animal is sleeping")

    def running(self):

        print("This animal is running")

#Child Class
#ChildClassName(ParentClassName)
class Rabbit(Animal):

    #Methods
    def run(self):

        print("Running!")  

class Fish(Animal):

    def swim(self):

        print("Swimming!")

class Eagle(Animal):

    def fly(self):

        print("Flying!")

  

#Creating Objects
rabbit = Rabbit()
fish = Fish()
eagle = Eagle()

#Assigning Values
print(rabbit.alive)
print(fish.alive)
print(eagle.alive)

print()

#Adding Methods
print("For Rabbits:")

rabbit.eat()
rabbit.sleep()
rabbit.run()

print()

print("For Fish:")
fish.eat()
fish.sleep()
fish.swim()

print()

print("For Eagle:")
eagle.eat()
eagle.sleep()
eagle.fly()

print()

```

---

## Multilevel Inheritance

It is when a *class* **inherits** from a **child class** becoming a *"grandchild class"* ( derived class )

```python

#Multi-Level Inheritance
  
#Parent Class with identifier name: Organism
class Organism:

    #Attribute
    alive = True
  
#Child Class
#Class "Animal" inherits data from Class "Organism"
class Animal(Organism):

    #Methods of Class "Animal"
    def eat(self):

        print("This animal is eating!")
        
#GrandChildren Class ( Derived Class )
#Class "Dog" inherits data from Class "Animal"
class Dog(Animal):

    #Methods of Class "Dog"
    def bark(self):

        print("This dog is barking")

#Creating Objects
#Creates object "dog"
dog = Dog()

#Displaying Attributes
print(dog.alive)

#Adding Methods
dog.eat()
dog.bark()

```

---

S.Sunhaloo