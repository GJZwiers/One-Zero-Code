# List Methods
Remember when we looked at strings how we could call functions on a string? The same holds true for lists, although the functions we can use on lists are different.

What if we want to add an element to a list? We can use `append` to add to the end of the list:
```python
animals = ["Cat", "Dog", "Fish"]
snek = "Snake"
animals.append(snek)
```
Now the list has 4 items, and the last item `Snake` has index 3. How about adding it to the start of the list instead? We can do that with `insert`, where we provide the index to insert at (0) and the item to insert ("Snake"):
```
animals.insert(0, snek)
```

Let's say we only appended the "Snake" element. The list will look like ["Cat", "Dog", "Fish", "Snake"]. It happens to be in alphabetical order but what if want to reverse that? You guessed it, there is a `reverse` method for doing just so.
```python
animals = ["Cat", "Dog", "Fish", "Snake"]
animals.reverse()
print(animals) # ["Snake", "Fish", "Dog", "Cat"]
```

So maybe we do not wanted to add the "Snake" element after all. To remove it we can use `pop`. We can give it the index of the item we want to remove. However, if we don't provide an index `pop` will remove the last item by default, so let's do that:
```python
animals = ["Cat", "Dog", "Fish", "Snake"]
animals.pop()
print(animals) # ["Cat", "Dog", "Fish"]
```

Although there are many more useful list methods, it is time to move on to dictionaries.

<div style="text-align: right">
<a href="dictionary.html">Next</a> | 
<a href="list.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>