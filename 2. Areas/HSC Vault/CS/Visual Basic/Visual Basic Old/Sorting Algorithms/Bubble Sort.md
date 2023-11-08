---
alias: Bubble Sort
tag: vb.net
date: 15-06-2023
---

## What is a Bubble Sort Algorithm?

Bubble Sort which is also known as **sinking sort**

- It is the **simplest** sorting algorithms  that *repeatedly* steps through the input list item by item.
	- **Comparing** the *current* item to the one **after** it

## Advantages of Bubble Sort Algorithm:

1. It is very simple and popular
2. It is easy to code in program
3. Fast *if and only if* the list of items to be sorted is **small**

## Disadvantages of Bubble Sort Algoritm: 

1. **Slow** if list of item to be sorted **big**

---

# Code ( with 1D-Array ) :

### Template for Bubble Sort Procedure ( Ascending Order ):

```vbnet

'Let Array In Sub Main Have Identifier Name "Array"
' With size 5

Sub BubbleSort()

    'Declaring Procedure's Variable
    Dim x As Integer
    Dim y As Integer
    Dim temp As Integer

    'Actual Sorting Part
    For x = 0 To 5

        For y = 0 To 4

            If Array(y) > Array(y + 1) Then

                temp = Array(y)
                Array(y) = Array(y + 1)
                Array(y + 1) = temp

End Sub

```

>[!note]
> The $">"$ symbol means that the sorting algoritm will perfom a **Bubble Up**
> **Bubble Up:** Sorts the data in **ascending order**
> To **Bubble Down** use $"<"$ symbol

>[!warning]
>This is the *procedure* only
>This code will **only** perform the sorting and **not** *display* the array

### Template for Bubble Sort:

- This is a full template with [[Arrays in Visual Basic#One Dimensional Array ( 1D-Array )| 1D-Array]]

```vbnet

'Integrating 1D-Array With Bubble Sort

'Declaring Global Variables
Dim arrayData(9) As Integer
'1D-Array With Identifier Name "CarNames"
'Adding Counter That Works With 1D-Array Before BubbleSort() Is Applied
Dim i As Integer
'Adding a counter that works with the 1D-Array After BubbleSort() Has Been Applied
Dim j As Integer


Sub Main()

    'Adding Data to 1D-Array
    arrayData(0) = 10
    arrayData(1) = 5
    arrayData(2) = 6
    arrayData(3) = 7
    arrayData(4) = 1
    arrayData(5) = 12
    arrayData(6) = 13
    arrayData(7) = 15
    arrayData(8) = 21 
    arrayData(9) = 8

    'Displaying The Array Before BubbleSort
    Console.WriteLine("Output Before Bubble Sort:")

    For i = 0 To 9
        Console.WriteLine(arrayData(i))
    Next i 

    Console.ReadLine()

    BubbleSort()

    'Displaying The Array After BubbleSort
    Console.WriteLine("Output Before Bubble Sort:")
    For j = 0 To 9
        Console.WriteLine(arrayData(j))
    Next j

    Console.ReadLine()

End Sub

Sub BubbleSort()

    'Declaring Procedure's Variables
    Dim temp As Integer
    'Hold The Value That Is Being Swapped
    Dim x As Integer
    'Refer To Pseudocode - Acts Like The "Step" Variable
    Dim y As Integer
    'Refer To Pseudocode - Acts Like The "Index" Variable

    For x = 0 To 9 'ArraySize Is 9
        For y = 0 to 8 'ArraySize - 1
            If arrayData(y) < arrayData(y + 1) Then
                temp = arrayData(y)
                arrayData(y) = arrayData(y + 1)
                arrayData(y + 1) = temp
            End If
        Next y
    Next x
    
End Sub

```

>[!note]
> The $">"$ symbol means that the sorting algoritm will perfom a **Bubble Up**
> **Bubble Up:** Sorts the data in **ascending order**
> To **Bubble Down** use $"<"$ symbol to sort data in **descending order**

>[!success]
> This code works!