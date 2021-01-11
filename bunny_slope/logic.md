# If I Were a Programmer.. - Logic

Programs need logic more often than not. Without logic, how would we tell a program what choices to make? 

Before we start with logic, we need to talk about **keywords**. These are words in a programming language that have been reserved for special purposes. As such, we cannot use keywords in variable or function names.

One of the most common keywords in Python is **if**. We can use it to check if a certain condition is true or false.
```python
isHappy = True

if happy:
    print("Yay!")
```

Note the syntax here. We write `if` and follow with a condition, then end the line with a colon (`:`). In Python, the line(s) following an `if` statement need to be indented. This is important for Python to understand the code.

What if we do not happen to be happy? We can write an `else` after the `if`:
```python
if isHappy == True:
    print("Yay!")
else
    print("Nay!")
```
What does double equals `==` mean? You already know that we use a single `=` to assign values to variables, but `==` is used to check equality. If the value on the left hand side of the operator is equal to the one on the right hand side, the code inside the statement will execute.


Lastly, we can add more checks to `if/else` constructs by using `elif` (else if) keywords in between:
```python
isHappy = False
isSad = False
isCrazy = True

if isHappy == True:
    print("Yay!")
elif isSad == True:
    print("Sob!")
elif isCrazy == True:
    print("Woop!")
else
    print("No feelings found.")
```

<div style="text-align: right">
<a href="bool-operators.html">Next</a> | 
<a href="booleans.html">Previous</a> | 
<a href="index.html">Home</a>
</div>