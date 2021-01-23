# Store All The Things! - Lists

If we need to store many values in Python we can declare a list. The following code creates an empty list by writing brackets `[]` and stores it in a variable:
```python
myList = []
```
We can also create a list with some initial values. Note that comma's are used to separate list items:
```python
animals = ["Cat", "Dog", "Fish"]
```

Every item in a list has an index, which is a number that is used to access that item. Indexes are numbered starting at zero. So, to access the first item in the list above, we would write animals[0], and animals[1] for the next item, and so on.
```python
print(animals[0]) # prints Cat
print(animals[2]) # prints Fish
```

Now we will learn a new function to get the length of a list: `len`. The list has 3 elements so it is easy in this case, though many times a list is larger and we cannot tell just by looking.
```python
len(animals)
```
A good thing to remember about lists is that the last element is always the length of the list minus one. The next piece of code will print the last index of the list, which contains `"Fish"`:
```python
lastItem = len(animals) - 1
print(animals[lastItem])
```

<div style="text-align: right">
<a href="list-2.html">Next</a> | 
<a href="try-except.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>