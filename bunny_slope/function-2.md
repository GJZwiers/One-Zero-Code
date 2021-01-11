# Functions, Part Two
In the previous section we defined the following function:
```python
def square(num):
    return num ** 2
```

Something about this function is not so great. The value `2` is _hardcoded_ into it, meaning if we wanted to reuse this function to, for example, raise a number to a higher exponent, we could not. Let's change that by adding another parameter, `exp`, and renaming the function to `raise_to_power`. Don't confuse this with `rise_to_power`, which is a function the cyborgs will use when they are ready..
```python
def raise_to_power(num, exp):
    return num ** exp
```
Now we can square any number, or cube it, you name it. However, now when we want to just square something we have to provide the exponent explicitly:
```python
raisePwr(3, 2):
```

It would be nice if we could set the `exp` parameter to a default value like `2`, so the default behavior of the function is to square the number if we do not provide a second argument. Here is how we assign a default value to a function parameter:
```python
def raise_to_power(num, exp = 2):
    return num ** exp
```
Now we can square a number like we did before, but also raise numbers to higher powers should we need to do so:

```python
three_squared = raise_to_power(3)
two_cubed = raise_to_power(2, 3)
```

<div style="text-align: right">
<a href="function-2.html">Next</a> | 
<a href="function.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>