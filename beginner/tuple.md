# Tuple Trouble

A tuple is another type of collection in Python. We saw that lists are _ordered_ and _changeable_ (we can add or remove elements) and that dictionaries are _unordered_ and changeable. Tuples are ordered and _unchangeable_. 

We declare a tuple with parentheses:
```python
example_tuple = (1, 2, 3)
```
Just like a list, we can access values in the tuple with indexes. For example, `example_tuple[0]` will give the value `1`. However, we cannot change the tuple and say `example_tuple[0] = 2`, or add/remove one of the elements. Tuples are useful when the data we are working with will have a fixed size. 

Tuples can contain values of different types as well:
```python
diverse_tuple = (1, True, "three")
```

<div style="text-align: right">
<a href="set.html">Next</a> | 
<a href="dictionary.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>