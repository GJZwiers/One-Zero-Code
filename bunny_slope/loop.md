# Oops I Did It Again - Loops

Often when writing programs we have to do a certain thing a lot of times. This is where programming languages provide **loops** to save us from having to write out instructions manually.

```python
on = True
i = 0

while on:
    i = i + 1
```
The code above shows a **while** loop. This type of loop will keep executing while a certain condition is true. Notice that we made a variable called `i` and set it to 0 initially. `i` is an _iteration variable_, a counter that increases as a loop is running. While the variable `on` is `True`, the program will loop and increase `i` by 1 each time.

One problem though: our loop will never stop. To fix this we need to add logic that determines when to set `on` to `False`. For example, when `i` reaches `100`. Let's also print the value of `i` each time and a message when the loop is done.
```python
on = True
i = 0

while on:
    print(i)
    i = i + 1
    if i == 100:
        on = False

print("Loop completed.")
```
Now we have a program that goes from 0 to 100 pretty fast!

[Next](for-loop.md)