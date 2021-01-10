# Do Not Repeat Yourself

Programmers try to avoid repetition in code because it is inefficient. One way to do so is by using **variables**. Variables allow you to store data for use at different points in time in the program. Open your editor and make a Python file with the following code:

```python
print("Happy Birthday To You!")
print("Happy Birthday To You!")
print("Happy Birthday, Dear User, Happy Birthday To You!")
```

There is repetition in this code. The text 'Happy Birthday To You!' is printed a couple of times. Right now this also means the computer needs to recreate that data anew every time. With a variable we can create the value once and reuse it. We can _declare_ a variable by giving it a name and a value. In programming languages the `=` sign is used to assign values to variables. Write the following at the top of the code:

```python
text = "Happy Birthday To You!"
```

We have now assigned the value "Happy Birthday To You!" to the variable `text`. Now we can use this value as the input for the `print` commands:

```python
text = "Happy Birthday To You!"

print(text)
print(text)
print("Happy Birthday, Dear User, Happy Birthday To You!")
```

You may have noticed that the text we put in the variable is also the last part of the third `print` call. Can we use our variable there too? Yes! It is possible to combine two parts of text using a `+` sign:

```python
text = "Happy Birthday To You!"

print(text)
print(text)
print("Happy Birthday, Dear User, " + text)
```

Now the value "Happy Birthday To You!" is created only once, stored in a variable `text` and reused three times in the `print` calls.

Another benefit of variables is the fact that we can give them a name. Giving data clear and descriptive names is a big benefit, especially in larger, more complex programs.

[Next](say-what-you-mean.md)