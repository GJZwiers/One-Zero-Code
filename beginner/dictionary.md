# D is for Dictionary

A dictionary is a data structure that allows you to access a value by looking up its key. These combinations are called _key-value pairs_. We declare an empty dictionary in Python by using curly braces `{}`. Then, we can add key-value pairs by writing the key first followed by `:` and finally the value. Comma's are used to separate multiple pairs:
```python
person = {
    "name": "Jennifer"
    "job": "Doctor",
    "education": "University" 
}
```
As you can see dictionaries allow us to group a lot of variables together in one structure. It would be a hassle to do it with individual variables, especially if the number of variables were to increase.
```python
name = "Jennifer"
job =  "Doctor",
education = "University"
```

Note that the values in a dictionary can be of any type:
```python
person = {
    "name": "Jennifer"
    "job": "Doctor",
    "education": "University"
    "degrees": ["High School", "College", "Medical School"],
    "number_of_cats": 1
    "married": False
}
```

To access one of the keys in the dictionary what we can do is write the name of the variable holding it and then the name of the key in brackets:
```python
person["name"]
```

Dictionaries are useful to store related data that does not need to be in a specific order. This as opposed to a list where the elements are ordered through the use of indexes.

<div style="text-align: right">
<a href="tuple.html">Next</a> | 
<a href="list-2.html">Previous</a> | 
<a href="../index.html">Home</a>
</div>