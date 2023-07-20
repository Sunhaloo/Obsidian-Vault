---
alias: Exception Handling in Python
tag: python
date: 03-07-2023
--- 

---

## List Of Contents:

- [[Exception Handling in Python#What is Exception Handling? | What is Exception Handling?]]
- [[Exception Handling in Python#Example: | Example]]

---

# What is Exception Handling?

It is an event detected *during* execution that **interrupts** the flow of the program

It is used in places like:

- Division by zero
- User entered data of another datatype

### Example:

```python

print("Division")

print()

try: #Exception Handling

    numerator = float(input("Enter A Value:"))

    denominator = float(input("Enter A Value: "))

    division = numerator / denominator

except ZeroDivisionError as e: #Will only check div by 0 # as e will print the exeption used

    print(e)

    print("Cannot divide by 0")

except ValueError as e: #Will only check values entered # as e will print the exeption used

    print(e)

    print("Enter Numbers Please!")
  
except Exception as e: #Will perform a general check # as e will print the exeption used

    print(e)

    print("Something went wrong!")

else:

    print(division)

finally: #This will always execute whatever the case might be
  
    print("This is needed and will always execute")

print()

```

S.Sunhaloo