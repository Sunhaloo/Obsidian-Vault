---
alias: Text Files in Python
tag: python
date: 03-07-2023
---

---

## List Of Contents:

- [[Text Files in Python#What is a Text File? | What is a Text File?]]
- [[Text Files in Python#File/Directory Detection | File/Directory Detection]]
- [[Text Files in Python#Check if File/Directory | Check if File/Directory]]
- [[Text Files in Python#Reading a File | Reading a File]]
- [[Text Files in Python#Creating and Writing Data Into Files in the Same Code | Creating and Writing Data Into Files in the Same Code]]
- [[Text Files in Python#Appending Data to File | Appending Data to File]]

---

# What is a [Text File](https://en.wikipedia.org/wiki/Text_file)?

A text file is a kind of computer that is structured as a sequence of lines of electronic text.

--- 

>[!Warning]
>To use text files; we need to type *"import os"* at the start of the code

## File/Directory Detection

It checks whether or not a file/directory exists

Format:

- os.path.exist(x)
	- Where x is the location of the file/directory

```python

#File/Directory Detection

#Importing OS Module
import os

if os.path.exists("D:/TextFile.txt"): #Checks if file exists

    print("Exists")

#OR

if os.path.exists(path): #Checks if file exists

    print("Exists")

```

## Check if File/Directory

It checks whether file is a *"file"* or *"directory"*

Format:

- For Files
	- os.path.isfile(x)
		- Where x is the location of the file

- For Directories
	- os.path.isdir(x)
		- Where x is the location of the directory

```python

path = "D:/TextFile.txt"
path1 = "D:/Folder"

  

if os.path.exists(path): #Checks if file exists

    print("Exists")


    if os.path.isfile(path1): #Checks if file is a "file"

        print("That is a file!")

    elif os.path.isdir(path1): #Checks if folder is a "folder"
  
        print("That is a folder/directory")

else:

    print("Does NOT Exists!")

print()

```

## Reading a File

It read a text file and outputs the contents of the text file

### Code:

```python 

#Reading File

#Import OS Module

try: # Exception Handling

    with open(path) as file: #Opening File for read ( automatically with this code and file closes automatically )

        print(file.read())
        
        #Will close file automatically

    print(file.closed) #Checks if whether file has been closed
    
except FileNotFoundError: # If file not found

    print("That file was not found")
    
print()

```

## Creating and Writing Data Into Files in the Same Code

### Code:

```python

#Writing Data Into Files

#Import OS Module
import os

with open("D:/textfile.txt", "w") as file: #Opening File for write ( automatically with this code and file closes automatically )

        for x in range(5):

                file.write("Hello\n")

                #"/n" is used to write on another line

        print(file.closed) #Checks whether file is closed

        file.close() #Closes file

        print(file.closed) #Checks whether file is closed
print()

```

## Appending Data to File

>[!warning]
>The file does **not** need to be **already** *created*

### Code:

```python

#Appending Data To File

#Import OS Module
import os

text1 = "This is another line after creating\n This is me appending"

with open('D:/test.txt', 'a') as file:

    file.write(text1)

    print(file.closed)

    file.close()

    print(file.closed)

print()

```

S.Sunhaloo