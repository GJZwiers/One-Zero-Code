# Strings

In the previous sections we have seen that text in computer programs has to be quoted. Or does it? Let's see what happens when we don't.

Write the following Python in a new file in your editor. I'll call it `strings.py`. This time, print any text you like but don't put it in quotes:

```python
print(Hi!)
```

Now run this program on the console. Go to your working directory `repos` and run:
```
python strings.py
```

Most likely you get back an error saying `SyntaxError: invalid syntax`. Computers need data to have a **data type** to understand how to work with it. The data type for text is **string** and strings are indicated with quotes. We can use single or double quotes: `'I am a string'` and `"I am a string"`. As a good practice, use single quotes for single characters like `'a'` and double quotes for anything else like `"Boomer"`.

Let's restore program function and move on. But don't worry, no strings attached! ;)

```python
print("Hi!")
```

[Next](strings-2)