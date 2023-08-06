---
alias: Text File
tag: vb.net
date: 16-06-2023
---

---

## List of Contents

- [[Text File in Visual Basic#What is a Text File?| What is a Text File?]]
- [[Text File in Visual Basic#Creating a Text File Only| Code to Create a Text File ( Blank Text File )]]
- [[Text File in Visual Basic#Creating a Text File and Writing One Line of Text Into File| Code to Create a Text File ( Writing a Line Into Text File )]]
- [[Text File in Visual Basic#Creating a Procedure That Can Be Called To Create a Text File| Code to Create a Text File ( By Using Procedure )]]

---

# What is a Text File?

A text file is a kind of computer that is structured as a sequence of lines of electronic text.

> From [Wikipedia](https://en.wikipedia.org/wiki/Text_file)

--- 

# Creating a Text File Only

## Code:

This code will create a text file called "TextFile" which will be stored at desired *location*

```vbnet


'File Class - Do NOT forget to write "Imports System.IO" as it tell VB that we are working with 'Text Files'

Imports System.IO

Module ModFiles
'If program does not work; then revert back to "Module Program"

	Sub Main()

		'Declaring Variables
		Dim FileWriter As StreamWriter
		'"FileWriter" is a Variable with Data Type "StreamWriter";
		'The Variables Name could have been anything

		FileWriter = File.CreateText("Location")
		'If you are placing file into another folder like D:\Folder1\TextFile.txt
		'Make sure that the folder is already created

		'Closing File - so that it does not stay in RAM
		FileWriter.Close()
		
	End Sub

End Module


```

>[!info]
>This will **not** write anything into the file.
>This code will **only** *create* a text file

# Creating a Text File and Writing One Line of Text Into File

## Code:

This code will create a text file called "TextFile" which will be stored at desired *location*. 

```vbnet

'File Class - Do NOT forget to write "Imports System.IO" as it tell VB that we are working with 'Text Files'

Imports System.IO

Module ModFiles
'If program does not work; then revert back to "Module Program"

	Sub Main()

		'Declaring Variables
		Dim FileWriter As StreamWriter
		'"FileWriter" is a Variable with Data Type "StreamWriter";
		'The Variables Name could have been anything

		FileWriter = File.CreateText("Location")
		'If you are placing file into another folder like D:\Folder1\TextFile.txt
		'Make sure that the folder is already created

		'Writing a Line Into Text File
		FileWriter.WriteLine("This is a line!")

		'Closing File - so that it does not stay in RAM
		FileWriter.Close()
		
	End Sub

End Module

```

### Creating a Procedure That Can Be Called To Create a Text File

```vbnet


'File Class - Do NOT forget to write "Imports System.IO" as it tell VB that we are working with 'Text Files'

Imports System.IO

Module ModFiles
'If program does not work; then revert back to "Module Program"

	Sub Main()

		'Calling the Procedure TextFileCreator - To create a text file
		Call TextFileCreator()

	End Sub

	Sub TextFileCreator()

		'Declaring Procedure's Variables
		Dim FileWriter As StreamWriter
		'"FileWriter" is a Variable with Data Type "StreamWriter";
		'The Variables Name could have been anything

		FileWriter = File.CreateText("Location")
		'If you are placing file into another folder like D:\Folder1\TextFile.txt
		'Make sure that the folder is already created

		'Writing a Line Into Text File
		FileWriter.WriteLine("This is a line!")

		'Closing File - so that it does not stay in RAM
		FileWriter.Close()
		
	End Sub

End Module

```