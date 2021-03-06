# Say What You Mean

Let's have another look at the Python program from the previous section:
```python
text = "Happy Birthday To You!"

print(text)
print(text)
print("Happy Birthday, Dear User, " + text)
```

We have a variable named `text` with a birthday message in it. Imagine this program was much larger and another programmer had to work with this variable without knowing its exact contents. Would `text` suffice in that case? No. `text` is too vague, it does not convey the meaning of the value stored in the variable. It does not contain just any kind of text, it contains a birthday wish. 

Let's change the name of the variable. We cannot use spaces in variable names, so we will use underscores to link multiple words. This style to name variables is called **snake_case**:
```python
birthday_wish = "Happy Birthday To You!"

print(birthday_wish)
print(birthday_wish)
print("Happy Birthday, Dear User, " + birthday_wish)
```

Another type of casing is called **camelCase** where the first character of every word except the first is written in uppercase:
```python
birthdayWish = "Happy Birthday To You!"

print(birthdayWish)
print(birthdayWish)
print("Happy Birthday, Dear User, " + birthdayWish)
```

Always give your variables clear and descriptive names. It will help you when you return to work on a project after a long break where you may have forgotten its details. It will also help other programmers you might be working together with to understand your meaning. Always _say what you mean_.

<div style="text-align: right">
<a href="comment.html">Next</a> | 
<a href="dont-repeat.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>