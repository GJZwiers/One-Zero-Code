# Boolean Operators

Aside from equality we can check more conditions using logical operators. For example, we can check if one value is bigger or smaller than another:
```python
a = 1
b = 2

if b > a:
    print("b is bigger than a")
```

We can also explicitly check if two values are _not_ equal by writing `!=` instead of `==`:

```python
if a != b:
    print("The values are not equal")
```

Checking more than one condition at a time is also possible. We can use the `and` as well as `or` keywords with `if` to do so. Also good to know is that these are often written as `&&` and `||` in other programming languages.

```python
a = 1
b = 2
c = 3

if a < b and b < c:
    print("b is a number between a and c")

if a == 3 or b == 3 or c == 3:
    print("One of these numbers is 3")
```
