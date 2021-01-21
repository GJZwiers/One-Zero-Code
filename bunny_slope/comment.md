# Would You Like To Weigh In? - Comments

When we are programming it can sometimes be helpful to write comments in the code to provide more clarity to anyone who might read it at some point. In python a comment can be written by adding a `#` before the text:
```python
# This is a comment.
```

Any comments in the code will not be executed by Python when the code is run. Remember though that the first line in writing understandable code is to use clear and descriptive variable names. In other words, don't create a vague variable name and then write comments about what it does if you don't need to. For example, the following is not great:
```python
# This date means my birthday.
day = '01-06-2020'
```
Something like this would be much better:
```python
birthday = '01-06-2020'
```

Can you see the difference between the two code samples? In the first sample the variable is named ambiguously to `day`, which is quite generic and could mean any kind of day, requiring a comment to explain. The second sample, however, is clearly named and the variable `birthday` immediately conveys its meaning.

<div style="text-align: right">
<a href="input.html">Next</a> | 
<a href="say-what-you-mean.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>