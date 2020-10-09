# Working with Basic Data Types
> In this guide you will learn about the basic types of data used in programming and how to cast one type to another.

In the previous part of the course you already encountered a few data types: **strings**, **integers** and **booleans**. These are basic types that are used quite a lot. We will cover them in more detail here.

## Booleans
The simplest type of data is probably the boolean with the values `true` or `false`. It can be represented in memory by just one bit where `0` stands for true and `1` for false. In certain languages the values are written with the first character capitalized: `True` and `False`.

A boolean is often used as a flip switch in programs, where it is declared with a starting value and then changed under some condition to control the program flow. 

```
```
---
## Strings
Strings are the data type of text. A string value is made by writing it in quotes. Some languages accept single and double quotes while others reserve single quotes specifically for a single _character_.  
Computers understand text as a sequence of individual characters. Therefore each one of them in a string has a numeric **index** to represent its position with the first index being `0`. A character in a string can be accessed by writing its index number between square brackets, for example: `myString[0]`.

The sample below will print the character `i` to the screen:
```python
caesar_says = "Veni, Vidi, Vici"
print(caesar_says[3])
```

Strings can also be empty. This can be convenient when a string needs to be built through some program logic at a later stage. An **empty string** is declared using just quotes:
```python
empty_string = ""
```

Programming languages usually offer many built-in functions for strings, such as one to join two or more strings together, to make all characters uppercase or lowercase, and to search for specific text in a string.

---
### String Interpolation
A common concept is to insert values from variables into a string. This is called **string interpolation**. The values are often automatically cast to a string type if possible. The syntax for string interpolation differs a little across languages. The _common part_ is to place the variables to be inserted in curly brackets `{}` and to make the program recognize the string as interpolated through some syntax change. This can be done in many different ways depending on the language. Below are some samples:

Python
```python
age = 5
print(f'Angie is {age} years old.')
```

JavaScript
```javascript
let age = 5;
console.log(`Angie is ${age} years old.`);
```

C#
```csharp
int age = 5;
Console.WriteLine($"Angie is {age} years old.");
```

Rust
```rust
let age: i32 = 5;
println!("Angie is {} years old.", age);
```

### Strings with Date and Time
Sometimes it is helpful to have a timestamp in programs, for example to record the time a user of an app registered or logged in last. Time can be formatted as a string, usually with a system of special codes to indicate different components of date and time such as month, year or hour of day. 

Let's see how we can get the current time and format it into a string. Note that this example uses the concept of _chaining_, where two or more functions are called right after each another instead of writing them on multiple lines. The return of every function in the chain is put into the variable for the next function to work on.

```python
from datetime import datetime

current_time = datetime.now().strftime()
```

## Numbers
The number types used most often are the integer and the floating point number(float). The former is a whole number like `1` while the latter has one or more significant digits on the right side of the point like `2.5`.
Using integers or floats depends on the context. Integer values require less memory and can be processed faster. Floats need more memory but also offer more precision.



### Signed/unsigned 

Signed integers are numbers with a plus or minus sign. Unsigned integers can only be positive.


## Type Evaluation


## Casting to a Different Type

In addition, many other types in programming languages can be cast down to an equivalent boolean value when they have to be compared. An empty string, for example, is often casted down to `false` while any non-empty string is casted to `true`.
