---
alias: Stack ( Abstract Data Types )
tag: vb.net
date: 23-06-2023
---

---

## List Of Contents:

- [[Stack ( Abstract Data Types )#What is a [Stack](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))? | What is A Stack?]]
- [[Stack ( Abstract Data Types )#Template | Template]]
- [[Stack ( Abstract Data Types )#Example of Stack Program Code | Example of Stack Program Code]]

---

# What is a [Stack](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))?

A stack is an [[Data Structures ( Abstract Data Types )#What is an Abstract Data Type? | abstract data type]] that serves as a collection of elements, with two main operations 

- Push 
	- Adding Data/Element To Stack
- Pop
	- Removing Data/Element From Stack

It has **LIFO ( Last In First Out )** Structure

---

# Template

## Code:

```vbnet

'Template for Stack Program Code for Visual Basic

'These are the global variables

    Dim item As String
    Dim top As Integer
    Dim arrayStack(4) As String 'This is an array - NAME: arrayStack with UPPER BOUND = 4
    Dim i As Integer
    Dim count As Integer

    'This is the main program

    Sub main()

        'This is a user-defined PROCDEDURE

        createEmptyStack()

        Console.WriteLine("inserting items in stack")
        Console.WriteLine("")

        'This is a user-defined PROCDEDURE

        InsertItemStack("Ashley")
        InsertItemStack("lavind")
        InsertItemStack("Ashwin")
        InsertItemStack("Nishi")
        InsertItemStack("Atish")

        Console.WriteLine("")
        Console.WriteLine("Deleting an item in stack")
        Console.WriteLine("")

        'This is a user-defined PROCDEDURE

        removeItemStack()

        Console.WriteLine("")
        Console.WriteLine("inserting item in stack")
        Console.WriteLine("")

        'This is a user-defined PROCDEDURE

        InsertItemStack("Anusha")
        InsertItemStack("item5")

        Console.WriteLine("")
        Console.WriteLine("find an item in stack")
        Console.WriteLine("")

        'This is a user-defined PROCDEDURE

        findItem("lavind")

        Console.WriteLine()
        Console.WriteLine("printing elements in stack")

        For i = top To 1 Step -1
            Console.WriteLine(arrayStack(i))
        Next

        Console.Readkey()

    End Sub

    'This is a user-defined PROCDEDURE 

    Sub createEmptyStack()
        top = 0

    End Sub

    'This is a user-defined PROCDEDURE

    Sub InsertItemStack(ByVal item As String)

        If top = arrayStack.Length - 1 Then
            Console.WriteLine("overflow occurs")
        Else
            top = top + 1
            arrayStack(top) = item
            Console.WriteLine(item & " Inserted into stack")
        End If

    End Sub

    'This is a user-defined PROCDEDURE

    Sub removeItemStack()

        If top = 0 Then
            Console.WriteLine("Underflow")
        Else
            item = arrayStack(top)
            top = top - 1
            Console.WriteLine(item & " has been deleted")
        End If

    End Sub

    'This is a user-defined PROCDEDURE

    Sub findItem(ByVal item As String)

        For count = top To 1 Step -1

            If arrayStack(count) = item Then
                Console.WriteLine(item & "is found at position : " & count)
            End If
        Next

    End Sub

```

# Example of Stack Program Code 

- Create an Abstract Data Type ( STACK ) with
	- Array Name: FlowerStack
	- Array Size: 5
- Add the following items:
	- Rose
	- Bougainvillea
- Delete 1 item
- Add the following item:
	- Impatient
	- Shooting Star
- Display appropriate messages for all process
- Print/Output all of the data

```vbnet

Module Program

    'Declaring Global Variables

    'Object is the data we are adding
    Dim item As String
    '"top" is our pointer; which points to the current data item in array
    Dim top As Integer
    'Array with identifier name "FlowerStack"
    Dim FlowerStack(4) As String
    '"i" will be used to display the data in "FlowerStack"
    Dim i As Integer


    Sub Main()

        'Procedure with identifier name "CreateEmptyStack"
        CreateEmptyStack()

        'Telling the user that we are inserting item in Stack
        Console.WriteLine("Inserting Items In Stack:")
        Console.WriteLine("")

        'Inserting items into Stack
        InsertItemStack("Rose")
        InsertItemStack("Bougainvillea")

        'Telling the user that we are deleting/removing one item in Stack
        Console.WriteLine("")
        Console.WriteLine("Deleting An Item In Stack")
        Console.WriteLine("")

        'Deleting/Removing one item from Stack
        RemoveItemStack()

        'Telling the user that we are inserting item in Stack
        Console.WriteLine("")
        Console.WriteLine("Inserting Items In Stack")
        Console.WriteLine("")

        'Inserting items into Stack
        InsertItemStack("Impatient")
        InsertItemStack("Shooting Star")

        Console.WriteLine("")

        'Displaying Array 
        For i = top To 1 Step -1
            Console.WriteLine(FlowerStack(i))
        Next

        Console.ReadKey()

    End Sub

    'Creating Procedure 
    Sub CreateEmptyStack()

        top = 0

    End Sub

    Sub InsertItemStack(ByVal item As String)

        'Checking if top is full/already occupied
        If top = FlowerStack.Length - 1 Then

            Console.WriteLine("Stack Is Already Full")

        Else

            top = top + 1
            FlowerStack(top) = item
            Console.WriteLine(item & " has been inserted")

        End If

    End Sub

    Sub RemoveItemStack()

        If top = 0 Then

            Console.WriteLine("Stack Is Already Empty")

        Else

            item = FlowerStack(top)
            top = top - 1
            Console.WriteLine(item & " has been deleted")

        End If

    End Sub


End Module

```
