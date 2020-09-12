# Fundamentals - Programming

This page describes the basic concepts found in almost all programming languages. You will learn how to store values, do something lots of times, make decisions using logic and create code that is reuseable. Code examples for these concepts are provided in three languages: Python, JavaScript and Rust.

### On this page
1. [Storing Data in Variables](#storing-data-in-variables)
2. [Repeating Actions with Loops](#repeating-actions-with-loops)
3. [Controlling Program Flow with Logic](#controlling-program-flow-with-logic)
4. [Writing Functions for Reusable Behaviors](#writing-functions-for-reusable-behaviors)

## Storing Data in Variables

In programming, application data is stored in **variables**. Every variable has a _name_, a _type_, and a _value_. 

The **name** can be almost anything, although usually there are a few rules to follow and a couple of good practices to uphold. One good principle is simply to __say what you mean__ when naming variables. Programming is not like writing a novel, where you might choose words that are exceptionally beautiful, provocative and/or extravagant. When writing code we want to use names that are clear, concise and descriptive instead. This helps to provide clarity for both yourself and your fellow developers, both in the present and in the future.

**Types** are needed for the computer to understand how to work with a particular variable. Some common data types you'll come across are integers (whole numbers), floating point numbers, strings of text, booleans (true or false values) and more complex objects such as lists. Types can be **static** where the type of the variable is not permitted to change over the course of a program, whilst others have **dynamic** types which can. 

<details>
    <summary>More info on static vs. dynamic</summary>

    Using static types tends to have small performance benefits because compilers need to allocate more computer memory for dynamic variables to account for their changing nature.
</details><br>

The **value** of a variable is closely linked to its type. An integer value might be 2 or 1991. A string value might be 'Hello' or '2'. Notice something peculiar? Integers are written down as is but strings are surrounded with quotes. Now we have the integer value 2 and the string value '2'. Although the integer and the string have the same _value_ they do not have the same _type_. This can be of importance when working with numbers because computers cannot use strings in calculations right away.

When a value does not change, it is called a **constant**, as opposed to the _static_ unchanging type mentioned before. Constant values are often written in capitals to distinguish them from other numeric values.

Programming syntax has certain **keywords**. There words are reserved by the language for a certain task and cannot be used as a variable name. One example is the word `if` which is reserved for applying program logic.


### Examples

Variable declarations tend to have the following structure:
```
name = value
```
A language often uses some keyword such as `var` to declare the variable:
```
var name = value
```

##### v.1: General template to declare a variable.
```
[KEYWORD] [NAME] = [VALUE]
```

When a variable name has more than one word, we cannot use spaces. Instead, we can glue the words together and write the first character of every word after the first in uppercase. This style is called camel case, supposedly because of how the uppercase characters protrude from the text like humps on a camel's back:

```
var nameInCamelCase = ...
```

Another common style for variable names is snake case, which uses underscores between the words:
```
var name_in_snake_case = ...
```

Let's look at how you shouldn't name a variable. Check out the code below, which declares a variable with name 'Jimmy' and value '5' and then prints the text 'Jimmy is 5 years old' to a console window, using the value of the variable. The following code snippets make use of strings and variable interpolation, if you are not familiar on this topic see [Strings](strings.md).
```
var jimmy = 5;

console.log(`Jimmy is : ${jimmy} years old`);
```

The problem here is that although Jimmy is five, five is not Jimmy. Five is Jimmy's age. Let's change that:
```
var jimmiesAge = 5;

console.log('Jimmy is : {1} years old', jimmiesAge);
```
This is better. However, imagine there's someone else that's five years old as well, but not named Jimmy. We could write this:
```
var jimmiesAge = 5;

console.log('Jimmy is : {1} years old', jimmiesAge);
console.log('Angie is : {1} years old', jimmiesAge);
```
From a functional perspective this works fine, but this approach gets confusing quite fast. both Jimmy and Angie have a shared attribute, which is their age.

```javascript
var age = 5;

console.log(`Jimmy is ${age} years old`);
console.log(`Angie is ${age} years old`);
```

The samples thus far were written in the JavaScript programming language. Let's look at some other ones and see how they differ.

Python
```python
age = 5

print(f'Jimmy is {age} years old')
print(f'Angie is {age} years old')
```

C#
```csharp
int age = 5;

Console.WriteLine($"Jimmy is {age} years old");
Console.WriteLine($"Angie is {age} years old");
```

Rust
```rust
let age: i32 = 5;

println!("Jimmy is {} years old", age);
println!("Angie is {} years old", age);
```

### Concise versus precise

---

## Repeating Actions with Loops

On many occasions programmers need to perform an operation a number of times. When this number is small we can get away with writing it out by hand but when a certain action must be done a lot of times that gets tedious fast. To make life easier, programming languages use loops to do things many times.

Say we have a counter and want to count up to twenty. Without a loop the code might look like this:
```
counter = 0;

counter = counter + 1;
counter = counter + 1;
counter = counter + 1;
17 more times...
```

The first type is called a `for` loop and can be described as "do something a fixed number of times." For loops have an iteration variable with a starting value (usually 0), a condition that has to be true to keep looping, and how much the iterator increases each time. In a general sense `for` loops can be defined as:
```
for (START CONDITION, LOOP CONDITION, INCREMENT BY) {
    DO SOMETHING
}
```


JavaScript
```javascript
let counter = 0;    // let counter be 0

for (let i = 0; i < 20; i++) {
    counter = counter + 1;
}
```

The code above can be read as: "For a variable `i` that starts at `0`, while `i` is smaller than `20`, increment `i` _after_ adding `1` to `counter`". This is a fairly long syntax but it reveals how loops work. Other languages may use shorter syntax such as `for .. in ..`:

Python:
```python
counter = 0

for i in range(20):
    counter = counter + 1
```

Rust:
```rust
let mut counter: i32 = 0;

for i in 0..20 {
    counter = counter + 1;
}
```


---

## Controlling Program Flow with Logic

if else

---

## Functions

_A function performs a specific task with different inputs in multiple places._

Functions provide a means to reuse actions in multiple places. They are blocks of code that can take input, do something with it and return output. However, they can also take zero inputs and/or return no outputs at all. This is unlike mathematical functions which must have a unique output for every unique input.
In programming function inputs are called **parameters** and function outputs are called **return** values.


In most high-level languages functions consist of a keyword, a name, parameters and a function body enclosed in curly brackets. The keyword is specific to the language, for example `function`, `fn` or `def` (from `define`).

##### f.1: General template for defining a function. P stands for parameter.
```
KEYWORD NAME(P1, P2, ...) {

}
```
Inside the brackets you can use most other building blocks of code. You can declare and use variables, logic statements, loops and call upon other functions. Do notice that variables declared in a function are local to it, meaning they can't be accessed from the outside. When a function completes, these local variables are discarded.

Once defined, functions can be called. This is done by stating its name with parentheses and by entering values for the function parameters. Usually, parameters are called arguments when calling a function.

Returns

As an example, say we need to sum two numbers in various places in a program. Let's see what a `sum` function looks like in some different languages:

Python:
```python
def sum(a, b):
    return a + b
```

JavaScript:
```javascript
function sum(a, b) {
    return a + b;
}
```

Rust:
```rust
fn sum(a: i32, b: i32) {
    a + b
}
```
There are only minor differences between these languages. Python uses a colon and indentation to signal a code block, whereas the other two use curly brackets. Rust does not need an explicit `return` statement and requires type annotations in the function parameters (in this case an `i`nteger that takes `32` bits of memory space. For more information see [Numbers](numbers.md)). 




##### c.1: General template for defining a method.
```
XSMOD KEYWORD NAME(P1, P2, ...) {

}
```
