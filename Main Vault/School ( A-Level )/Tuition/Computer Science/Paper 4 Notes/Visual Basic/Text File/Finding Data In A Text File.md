---
alias: Finding Data In A File
tag: vb.net
date: 23-06-2023
---

---

## List Of Contents:

- [[Finding Data In A Text File#Searching Data in a Text File | Searching Data in a Text File]]
- [[Finding Data In A Text File#Example With Whole Text File | Example Of Searching Data]]

---

# Searching Data in a Text File

## Code:

This code will create a procedure that will be called to write more text in the file.

```vbnet

Module Program

	'Procedure with Identifier Name "FileSearch"
	Sub FileSearch()

		'Declaring Procedure's Variables
		Dim found As Boolean
		Dim count As Integer
		Dim x As StreamWriter
		Dim DataRetrieved As String
		Dim DataToFind As String

		'Initialising Variables
		count = 1

		'"Opening" File To Read'
		x = x.OpenText("Location")

		'Ask The User What Data Needs To Be Searched
		Console.WriteLine("Please Enter "Data" To Search: ")
		DataToFind = Console.ReadLine()

		'Reading File Until END OF FILE ( EOF )
		Do While x.Peek <> -1 

			'If Data Found
			DataRetrieved = x.ReadLine()

			If DataRetrieved = DataToFind Then

					'Output Confirmation That Data Has Been Found
					Console.WriteLine("Found At Line: " & count)
					found = True

			End If

		Loop

		'If Data NOT Found
		If found = False Then

			'Output Confirmation That Data Has NOT Been Found
			Console.WriteLine(DataToFind & " Not Found!")

		End If 

	End Sub

End Module

```

>[!note]
>This code is the **procedure only** - It will **not** *run* 
>This code need to be *called* in the main program 

# Example With Whole Text File

## Code

This code is a whole program that will

- Create a text file
- Write multiples lines into the text file
- Then *FileSearch()*  will be called into the main program
	- Which will **search** data into the text file

```vbnet

Imports System
Imports System.IO '--> To Be Able To Work With Text Files

Module Program

	Sub Main()

		'Declaring Variables To Create Text Files
		Dim Writer As Streamwriter

		'Creating Text File Called "Student.txt"
		Writer = File.CreateText("D:/Student.txt")

		'Writing Data Into Text File
		Writer.WriteLine("Hashim")
		Writer.WriteLine("Munir")
		Writer.WriteLine("Laifa")
		Writer.WriteLine("Nisaar")
		Writer.WriteLine("Mushir")
		Writer.WriteLine("Azhar")

		'Closing Text File ( Does Not Stay In RAM )
		Writer.Close()

		'Calling The Procedure With Identifier Name "FileSearch"
		Call FileSearch()

	End Sub

'Procedure with Identifier Name "FileSearch"
	Sub FileSearch()

		'Declaring Procedure's Variables
		Dim found As Boolean
		Dim count As Integer
		Dim x As StreamWriter
		Dim DataRetrieved As String
		Dim DataToFind As String

		'Initialising Variables
		count = 1

		'"Opening" File To Read'
		x = x.OpenText("Location")

		'Ask The User What Data Needs To Be Searched
		Console.WriteLine("Please Enter "Data" To Search: ")
		DataToFind = Console.ReadLine()

		'Reading File Until END OF FILE ( EOF )
		Do While x.Peek <> -1 

			'If Data Found
			DataRetrieved = x.ReadLine()

			If DataRetrieved = DataToFind Then

					'Output Confirmation That Data Has Been Found
					Console.WriteLine("Found At Line: " & count)
					found = True

			End If

		Loop

		'If Data NOT Found
		If found = False Then

			'Output Confirmation That Data Has NOT Been Found
			Console.WriteLine(DataToFind & " Not Found!")

		End If 

	End Sub

	
```