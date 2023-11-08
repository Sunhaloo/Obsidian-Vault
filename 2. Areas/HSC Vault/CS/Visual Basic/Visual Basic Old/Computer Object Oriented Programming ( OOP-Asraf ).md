---
alias: Computer OOP ( Asraf )
tag: vb.net
date: 29-06-2023
---

---

## List Of Contents:

- [[Computer Object Oriented Programming ( OOP-Asraf )#What is Computer Object Oriented Programming ( OOP )?| What is Computer Object Oriented Programming ( OOP )?]]
	- [[Computer Object Oriented Programming ( OOP-Asraf )#Example Of Computer OOP:]| Example Of OOP]]
	- [[Computer Object Oriented Programming ( OOP-Asraf )#Main Principles of Computer Object Oriented Programming| Main Principles]]
		- Encapsulation
		- Abstraction
		- Inheritance
		- Polymorphism
- [[Computer Object Oriented Programming ( OOP-Asraf )#Important: Step to take before writing anything!| Important: Step to take before writing anything!]]
- [[Computer Object Oriented Programming ( OOP-Asraf )#Examples of Computer Object Oriented Programming ( OOP ) Code|Examples of Computer Object Oriented Programming ( OOP ) Code ]]

---

# What is Computer Object Oriented Programming ( OOP )?

Object-Oriented Programming ( OOP ) is a style of programming characterised by the identification of **classes** of **objects** closely linked with **methods** with which they are associated

## Example Of Computer OOP:

A car is a good example to understand computer object oriented programming:

A car has a :

- Make
- Model
- Colour
- Manufactured Date
- Engine Size 

Hence, we would create a *Car* **object** with its *specifications* as **attributes**

## Main Principles of Computer Object Oriented Programming

1. Encapsulation
2. Abstraction
3. Inheritance
4. Polymorphism

# Important: Step to take before writing anything!
>[!warning] 
># Steps to take BEFORE writing any code:
> 1. After creating a *Console Aplication*
> 2. Select *"project"* and add a new class
> 3. Now there will be **2** files that can be worked on:
> *Program.vb* and *Class1.vb*

---

# Examples of Computer Object Oriented Programming ( OOP ) Code

## Example 1:

A bank customer is prompted for the following details for a new bank accout:

- Account Number
- Name
- Opening Balance

The program should:

1. Allow the customer to deposit and withdraw money
2. Display the new balance accordingly

## Writing Into "Class1.vb" file

```vbnet

'Check Notion Computer Object Oriented Programming Page'
'Example 1: Bank Account'

'Public Class with Identifier Name "BankAccount"'
Public Class BankAccount

  'Private Properties of Class "BankAccount"'
  Private AccountNum As String
  Private Name As String
  Private Balance As Decimal

  'Constructor to Initialise Properties/Attributes'
  'Identifier name for Constructor is always "New"
  'Setter'
  Public Sub New(ByVal a As String, ByVal n As String, ByVal b As Decimal)
    
    '"Public" Properties/Attributes'
    AccountNum = a
    Name = n 
    Balance = b 

  End Sub

  '"Public" Methods = Function/Procedures'
  'Getters'
  
  'Function with Identifier Name "GetAccountNum"'
  Public Function GetAccountNum() As String
    
    Return AccountNum
      
  End Function
  
  'Function with Identifier Name "GetName"'
  Public Function GetName() As String

    Return Name 

  End Function

  'Function with Identifier Name "GetBalance"'
  Public Function GetBalance() As String

    Return Balance
    
  End Function

  'User-Defined Procedures'
  'To Deposit Cash'
  Public Sub Deposit(ByVal Amount As Decimal)

    Balance = Balance + Amount

  End Sub

  'User-Defined Procedures'
  'To Withdraw Cash'
  Public Sub Withdrawal(ByVal Amount As Decimal)

    If Amount < Balance Then 

      'Welcome Page '
      Console.WriteLine("Welcome to BankName")

      'Withdrawing cash'
      Balance = Balance - Amount

    Else
        
      Console.WriteLine("Insufficient Amount in Bank xD(:")

    End If

  End Sub
  
  'Displaying Amount'
  Public Sub DisplayAccount()

    Console.WriteLine("Account Number: " & GetAccountNum())
    Console.WriteLine("Name: " & GetName())
    Console.WriteLine("Balance" & GetBalance())

  End Sub

End Class

```

## Writing Into "Program.vb" file

```vbnet

Module Program

  Sub Main()

    'Declaring Variables
    Dim MyAccountNum As String
    Dim MyName As Integer
    Dim MyBalance As Decimal

    'Asking the user to input his details
    Console.WriteLine("Please Enter Your Account Number: ")
    MyAccountNum = Console.ReadLine()

    Console.WriteLine("Please Enter Your Name: ")
    MyName = Console.ReadLine()

    Console.WriteLine("Please Enter Your Starting Balance: ")
    MyBalance = Console.ReadLine()

    'Instantiate the object MyAccount
    'New Account Takes the Datatype BankAccout( and passing the values that user wrote )
    Dim MyAccount As New BankAccount(MyAccountNum, MyName, MyBalance)

    Console.WriteLine("Opening Balance")
    'Calling the Procedure DisplayAccount to display account 
    MyAccount.DisplayAccount()

    Console.WriteLine()

    Console.WriteLine("A Deposit of Rs 500 has been effected")
    'Calling the Prodecure Deposit to deposit cash
    MyAccount.Deposit(500)
    'Calling the Procedure DisplayAccount to display account
    MyAccount.DisplayAccount()

    Console.WriteLine()

    Console.WriteLine("A withdrawal of Rs 1000 has been affected")
    'Calling the Prodecure Withdrawal to withdraw cash
    MyAccount.Withdrawal(1000)
    'Calling the Procedure DisplayAccount to display account
    MyAccount.DisplayAccount()

    'To be able to read output
    Console.ReadLine()
  End Sub

End Module

```