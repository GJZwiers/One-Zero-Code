# Bring Your Own Function

We have been using various _functions_ thus far, including `print`, `upper` and `range`. There are many more built-in functions in Python but we can also make our own. To do so we first have to write a function _definition_ which will tell the program what that function does and what _parameters_ the function has. When we make a call to the function the actual parameters we give it are called the  _arguments_. For example, when we made calls to `print` we gave a string to that function as an argument.

Let's define a function that takes a number and returns the square of that number. We start by writing the keyword `def` (for `define`), continue with the name of our new function, then end with a pair of parentheses and a colon:
```python
def square():
```
In between the parentheses we declare a parameter that is the number that the function will square. Let's call it `num`:
```python
def square(num):
```
On the next line we have to indent the code and actually square the number. If you recall from the section on number operators we can use `**`. Also, we want to return the squared number:
```python
def square(num):
    return num ** 2
```
Now we can call our new `square` function from code:
```python
def square(num):
    return num ** 2

ten = 10
ten_squared = square(ten)
print(ten_squared)
```

<div style="text-align: right">
<a href="function-2.html">Next</a> | 
<a href="for-loop.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>