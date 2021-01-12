# Working with Strings

Python has a number of built-in functions for strings that we can use in programs. For example, if we wanted to store a name in a database all in lowercase characters, we could call the `upper` function on a string. `upper` is a string function that changes all lowercase characters to uppercase. When we call a function _on_ something, we say _method_ instead of _function_.

How do we call a method _on_ a string? Write the name of the variable holding a string, follow it with a dot (`.`) and add the name of the method. Finally, place a pair of parentheses at the end to call it:
```python
name = "Marie-Anne Jones"
name = name.upper()
print(name)
```
Finally, we're calling something other than `print`, right? Oh wait, we're actually still calling `print`.. Well, atleast we're not _just_ calling `print` anymore!

Note the difference between the calls to `upper` and `print`. `upper` is called on the string `name` while `print` is called independently. Also note on the second line we _reassigned_ a value to `name` in order to store the new value from the `upper()` call. In programming we say that a function **returns** a value. The program will store the return value in our variable `name` and then print it to the console.

After the `upper` method completes the variable `name` should hold the value `"MARIE-ANNE JONES"`. Run the program to see if this is indeed the case.

We can also split a string. How can we do that? You guessed it, with the `split` function:

```python
name = "Marie-Anne Jones"
name_parts = name.split(' ')
print(name_parts)
```

Note we need to provide a character to split by, in our case spaces. The result of splitting `name` by spaces is not one but two strings (`Marie-Anne` and `Jones`) in a _list_. We will talk more about lists in Python in a later section.

Let's try one more string function: `find`. It is used to find a substring within a string. For example, we can try to find `one` in the string `Marie-Anne Jones`:

```python
name = "Marie-Anne Jones"
substring = "one"
name.find(substring)
```

If 'one' is found in `Marie-Anne Jones` the `find` function will return a number. This number is called an `index`. Every character in a string gets a number, starting at zero. If we run the code above the number `12` is returned by the `find` function, because that is the index, or location, of the first character of `one` in the string.

There is a lot more we can do with strings but first we are going to take a closer look at using numbers in Python.

<div style="text-align: right">
<a href="number.html">Next</a> | 
<a href="string.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>