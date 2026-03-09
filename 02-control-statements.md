# Control Statements in Python

Control statements allow a program to make decisions and execute different blocks of code depending on conditions.

They control the flow of execution in a program.

---

# Real-Life Example

Suppose you want to buy a movie ticket.

You have **100 rupees in your wallet**, but you are not sure if the ticket price is affordable.

We can use a condition to check whether we can buy the ticket.

```python
ticket_price = 90
wallet_size = 100

if ticket_price <= wallet_size:
    print("you can buy the ticket")
else:
    print("you cannot buy the ticket")
```

### Explanation

- The program compares the ticket price with the amount of money in the wallet.
- If the wallet has enough money, the program prints that you can buy the ticket.
- Otherwise, it prints that you cannot buy the ticket.

---

# Basic Syntax of If-Else

```python
if condition:
    # code to execute if condition is true
else:
    # code to execute if condition is false
```

---

# Multiple Conditions (If-Elif-Else)

Sometimes we need to check multiple conditions.  
For example, a grading system based on marks.

```python
marks = int(input("enter your marks: "))

if marks >= 90:
    print("A+")
elif marks >= 80:
    print("A")
elif marks >= 70:
    print("B")
else:
    print("C")
```

### Explanation

- `if` checks the first condition.
- `elif` checks additional conditions.
- `else` runs if none of the previous conditions are true.

---

# Python Keywords

Python has reserved words called **keywords** that cannot be used as variable names.

Example keywords include:

```
if, else, elif, for, while, break, continue, class, return
```

You can view all Python keywords using the `keyword` module.

```python
import keyword
print(keyword.kwlist)
```

This will display a list of all reserved keywords in Python.

---

# Summary

In this section we learned:

- What control statements are
- How `if` and `else` work
- How to handle multiple conditions using `elif`
- Real-life example using conditions
- Python reserved keywords
