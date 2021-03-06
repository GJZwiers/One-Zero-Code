# More on Loops

Another type of loop available in Python is the `for` loop. First recall the `while` loop we built in the previous section:
```python
on = True
i = 0

while on:
    print(i)
    i = i + 1
    if i == 100:
        on = False
```

As it turns out we can rewrite this as a `for` loop. We start with the keyword `for` and declare an iteration variable, for example `i`. Next, we write the keyword `in` and follow it with the number of times we want the loop to loop. Python has a function called `range` that can generate a range of numbers for us:
```python
for i in range(100):
    print(i)
```
Take a moment to compare the `for` loop code with the `while` loop. If you run both of these loops individually you can see that they accomplish the same.
`for` loops were designed to do automatically the things that we have to do manually with a `while` loop, such as increasing `i`.

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
<div class="mermaid">
stateDiagram-v2 
    [*] --> Start
    Start --> [*]
    Start --> Increment
    Increment --> Act
    Act --> Increment
    Act --> [*]
</div>

###### Diagram 1: A state representation of the for-loop

We can stop a loop early if we need to using the `break` keyword. The loop below will execute until it arrives at the number `13`:
```python
evilNumber = 13

for i in range(100):
    if i == evilNumber:
        break
    else 
        print(i)

print("Loop completed.")
```

<div style="text-align: right">
<a href="function.html">Next</a> | 
<a href="loop.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>