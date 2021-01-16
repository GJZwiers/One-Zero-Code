# Something went wrong.. - Errors

A large part of programming consists of encountering, identifying and solving errors. We have seen at least one so far, the syntax error that Python throws when we do not enclose a string in quotes.

But there are many more kinds of errors. For example, try to run the following code:
```python
x = 2 / 0
```
This throws a `ZeroDivisionError: division by zero` in Python, because dividing by zero is not possible in programming nor in mathematics.



If we were writing a function that divides numbers we could raise this error ourselves with the `raise` keyword, giving it a custom error message to give more specific information to the user:
```python
def divide(numerator, denominator):
    if denominator == 0:
        raise ZeroDivisionError('Divide: parameter "denominator" cannot be zero.')

    return numerator / denominator
```
Now, if someone using the program were to accidentally call something like `divide(2 / 0)` they would get a message telling them exactly what went wrong. In this case if we didn't include the error handling code Python would still have given a pretty good error message. However, this is not always the case. As a programmer, always try to think about what might go wrong in your code and handle errors appropriately.

<div style="text-align: right">
<a href="try-except.html">Next</a> | 
<a href="function-2.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>