---
alias: Appending Data Into A Text File
tag: vb.net
date: 22-06-2023
---

---

## List Of Contents:

- [[Appending Data Into A Text File#What is Appending? | What is Appending?]]
- [[Appending Data Into A Text File#Appending Data Into File ( Procedure Code Only ) | Appending Data Into File ( Procedure Code Only )]]
- [[Appending Data Into A Text File#Example With Whole Text File | Example Of Appending Data]]

---

# What is Appending?

Appending is to add ( something ) to the end of a written document

# Appending Data Into File ( Procedure Code Only )

## Code:

This code will create a procedure that will be called to write more text in the file.


```vbnet

'Procedure With Identifier Name = "FileAppend"
Sub FileAppend()

	'Declaring Procedure's Variables
	Dim x As StreamWriter

	'"Opening" File so that new line can be added
	x = File.AppendText("Location") 

	'Writing 1 line into the text file
	x.WriteLine("This is a line that has been added")

	'Closing Text File ( Does not stays in RAM )
	x.Close()

End Sub

```

>[!note]
>This code is the **procedure only** - It will **not** *run* 
>This code need to be *called* in the main program 

# Example With Whole Text File 

## Code:

This code is a whole program that will

- Create a text file
- Write multiples lines into the text file
- Then *FileAppend()*  will be called into the main program
	- Which will **add** new lines into the text file

```vbnet

'File Class - Do NOT Forget To Write "Imports System.IO"
'As We Are Working With Text Files
Imports System.IO

Module Program

Sub Main()

    'Declaring Variables
    Dim Writing As StreamWriter

    'Creating Text File Called "STUDENT"
    Writing = File.CreateText("D:/TextFile Programming/STUDENT.txt")

    'Inputting all of these name into STUDENT.txt
    Writing.WriteLine("Hashim")
    Writing.WriteLine("Munir")
    Writing.WriteLine("Laifa")
    Writing.WriteLine("Nisaar")
    Writing.WriteLine("Mushir")
    Writing.WriteLine("Azhar")

    'Closing Text File - STUDENT.txt
    Writing.Close()

End Sub


'Procedure With Identifier Name = "FileAppend"
Sub FileAppend()

	'Declaring Procedure's Variables
	Dim x As StreamWriter

	'"Opening" File So That New Line Can Be Added
	x = File.AppendText("D:/TextFile Programming/STUDENT.txt") 

	'Writing 1 Line Into Text File
	x.WriteLine("This is a line that has been added")

	'Closing Text File ( Does Not Stays In RAM )
	x.Close()

End Sub

```