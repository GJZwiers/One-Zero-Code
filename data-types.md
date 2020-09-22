# Working with Primitive Data Types
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

Programming languages usually offer many built-in functions for strings, such as one to join two or more strings together, to make all characters uppercase or lowercase, and to search for specific text in a string.

---
### String Interpolation
A common concept is to insert values from variables into a string. This is called **string interpolation**. The values are often automatically cast to a string type if possible. The syntax for string interpolation differs a little across languages. The _common part_ is to place the variables to be inserted in curly brackets `{}` and to make the program recognize the string as interpolated through some syntax change. This is done in different ways depending on the language. Below are some samples:

#### Samples - String Interpolation
Python
```python
age = 5
print(f'Angie is {age} years old.')
```

JavaScript
```javascript
var age = 5;
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
Sometimes it is helpful to have a timestamp in programs, for example to record the time a user of an app registered or logged in last. Strings that work with date and time 


## Numbers


## Type Evaluation


## Casting

In addition, many other types in programming languages can be cast down to an equivalent boolean value when they have to be compared. An empty string, for example, tends to be downcasted to `false` while any other string value is casted to `true`.