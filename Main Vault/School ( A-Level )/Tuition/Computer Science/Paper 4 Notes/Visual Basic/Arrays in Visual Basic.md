---
alias: Arrays
tag: vb.net
date: 08-06-2023
---

---

## List of Contents:

- [[Arrays in Visual Basic#What is an Array?| What is an Array?]]
- [[Arrays in Visual Basic#One Dimensional Array ( 1D-Array )| One Dimensional Array ( 1D-Array )]]
- [[Arrays in Visual Basic#Template ( Does Not Display Array ):| Template of 1D-Array ( Does NOT Display )]]
- [[Arrays in Visual Basic#Template ( Displays Array ):| Template of 1D-Array ( Does Display )]]

---

# What is an Array?

In computer science, an array is a 

- **Data structure** consisiting of a collection of *values* or *variables* of **same** memory size each by at least one array index. 
- Used in places where data need to be:

	1. Entered in a list
	2. Searched
	3. Sorted

- Alogorithms that uses array:

	- [[Bubble Sort]]

---

# One Dimensional Array ( 1D-Array )

- **Simplest** form of an array in which *values* are stored **linearly**
	- Which can be accessed *invidiually* by:
		- Pointing the *index* to the specific **address**

## Code: 

### Template ( Does Not Display Array ):

- Simple 1D-Array Code
- Datatype: Integer

```vbnet

Sub Main()
	
	'Declaring Variables
	Dim Array(9) As Integer
	'1D-Array With Identifier Name "Array"

	'Adding Data To The 1D-Array
	Array(0) = 20
	Array(1) = 3
	Array(2) = 4
	Array(3) = 8
	Array(4) = 12
	Array(5) = 99
	Array(6) = 4
	Array(7) = 26
	Array(8) = 4

	Console.ReadKey()
	'To Allow User To See Output Screen

End Sub() 

```

>[!warning]
>This code will **only** *create* an array.
>It will **not** *display* the array

- Simple 1D-Array Code
- Datatype: String

```vbnet

Sub Main()

    'Declaring Variables
    Dim Array(9) As String
    '1D-Array With Identifier Name "Array"

    'Adding Data To The 1D-Array
		Array(0) = "Liyana"
    Array(1) = "Mikhaeel"
    Array(2) = "Inaaya"
    Array(3) = "Rachel"
    Array(4) = "Ilhaan"
    Array(5) = "Rose"
    Array(6) = "Laydin"
    Array(7) = "Suraj"
    Array(8) = "Annabelle"

		Console.ReadKey()
		'To Allow User To See Output Screen

End Sub

```

>[!warning]
>This code will **only** *create* an array.
>It will **not** *display* the array

### Template ( Displays Array ):

- Simple 1D-Array Code
- Datatype: Integer

```vbnet

Sub Main()

	'Declaring Variables
	Dim TheArray(9) As Integer
	'1D-Array With Identifier Name "TheArray"
	Dim i As Integer
	'Adding A Counter That Works With The Array

	'Adding Data To The 1D-Array
	TheArray(0) = 52
	TheArray(1) = 58
	TheArray(2) = 14
	TheArray(3) = 2
	TheArray(4) = 100
	TheArray(5) = 5982
	TheArray(6) = 8
	TheArray(7) = 2
	TheArray(8) = 963
	TheArray(9) = 41
	
	'Displaying 1D-Array
	For i = 0 To 9
		Console.WriteLine(TheArray(i))
	Next i

	Console.ReadKey()
	'To Allow User To See Output Screen

End Sub

```

>[!success]
>This code is able **display** the array

- Simple 1D-Array Code
- Datatype: String

```vbnet

Sub Main()

    'Declaring Variables
    Dim CarNames(9) As String
    '1D-Array With Identifier Name "CarNames"
    Dim i As Integer
	'Adding A Counter That Works With The Array

    'Adding Data To The 1D-Array
    CarNames(0) = "Rx-7"
    CarNames(1) = "Supra"
    CarNames(2) = "AE-86"
    CarNames(3) = "GT-86"
    CarNames(4) = "GTR-R32"
    CarNames(5) = "McLaren-P1"
    CarNames(6) = "Porsche-918-Spyder"
    CarNames(7) = "Koenisegg-Regera-R"
    CarNames(8) = "Lancer-MR9"

		'Displaying The Array
    For i = 0 To 9 
        Console.WriteLine(CarNames(i))
    Next i

    Console.ReadKey()
    'To Allow The User To See Output Screen

End Sub

```

>[!success]
>This code is able **display** the array

# Two Dimensional Array ( 2D-Array )

- **Data structure** that contains a collection of *cells* laid out in a 2-dimensional grid
	- Has:
		- Rows
		- Columns

## Code:

### Template:

- Simple 2D-Array Code
- Datatype: Integer

```vbnet

Sub Main()

    '2D-Array ==> array2D(rows, columns)

		'Declaring Variables
    Dim array2D(2, 3) As Integer
    '2D-Array with identifier name "array2D"
    Dim row As Integer
    Dim column As Integer

    '2D-Array starts with 0 as well
    For row = 0 To 2
        For column = 0 To 3
            array2D(row, column) = 1
            'fills the array with value "1"
        Next
    Next

		Console.ReadKey()
		'To allow the user to see output screen

End Sub

```

>[!warning]
>This code will **only** *create* an array.
>It will **not** *display* the array

- Simple 2D-Array Code
- Datatype: Integer

```vbnet

    Sub Main()

        'Declaring Variables
        '2D-Array ==> array2D(rows, columns)
        Dim array2D(2, 3) As Integer
        '2D-Array With Identifier Name "array2D"
        Dim row As Integer
        Dim column As Integer

        '2D-Array Starts With 0 As Well
        For row = 0 To 2
            For column = 0 To 3

                Console.WriteLine("Please Enter a Value: ")
                array2D(row, column) = Console.ReadLine()

            Next
        Next

        'Displaying Array
        For row = 0 To 2
            For column = 0 To 3
                Console.WriteLine("row = " & row & " column = " & column & " data in array is: " & array2D(row, column))
            Next column
        Next row

    End Sub

```

>[!success]
>This code is able to **display** the array

