# Fundamentals - Programming

> In this guide you will learn how to store values, do something lots of times, make decisions using logic and create reusable actions. 

### On this page
1. [Storing Data in Variables](#storing-data-in-variables)
2. [Repeating Actions with Loops](#repeating-actions-with-loops)
3. [Controlling Program Flow with Logic](#controlling-program-flow-with-logic)
4. [Reusing Behavior with Functions](#reusing-behavior-with-functions)

---

Four basic concepts are found in almost all programming languages: **variables**, **loops**, **logic** and **functions**. However, code can be written without any of them. Let's start like that and see the use of each concept along the way.

Imagine a grocery store where the owner has a computer linked to a big screen to display items on sale. Programming languages can print text to a screen called the **console**. Every language has a command built-in for this, for example in Python it is called `print`. We can use it by typing `print` followed by parentheses and by placing the text we want to print in between, in quotes. The store owner is showing the console on the big screen and can print a welcome message for his customers:
```python
print("Welcome!")
```
After welcoming, the owner wants to show the special offer of the day. For promotion he displays it a couple of times by writing more `print` commands, each one on a new line:
```python
print("2 oranges for the price of 1!")
print("2 oranges for the price of 1!")
print("2 oranges for the price of 1!")
```
Note that the program is printing the same text more than once. In programming this means the computer has to create the same value anew each time. This makes the program somewhat inefficient, and the code starts looking repetitive. Fortunately there is a good solution: using a _variable_. 

## Storing Data in Variables

In programming, application data is stored in **variables**. Every variable has a _name_, a _type_, and a _value_. We can access the value by referring to the name.

The **name** can be almost anything, although usually there are a few rules to follow and a couple of good practices to uphold. One good principle is simply to __say what you mean__ when naming variables. Programming is not like writing a novel, where you might pick words that are exceptionally beautiful, provocative or extravagant. When writing code we want to use names that are clear, concise and descriptive instead. This helps both yourself and your fellow developers in the present as well as the future.

**Types** are there so the computer understands how to operate on different data. For example, adding two numbers together is different than adding two text sentences together. Furthermore, types differ in how much memory space they take.

The **value** a variable can have is closely linked to its type. A numeric value might be `2` or `1991`. A text value might be `"Hello"` or `"2"`. Do you notice anything peculiar? The numbers are written down as is but the text is enclosed in quotes. That is because the numbers are of the _integer_ type while text is of type _string_.  
Why does this matter? Let's say we have a variable with the value `"2"`. Although it is a number, its type is not, and computers can only do calculations with numeric types. The value needs to change type which in programming is called **casting**. Some languages will automatically cast strings to integers in calculations but in others you will have to explicitly tell the program to do so.

Languages differ in how flexible they are in changing variable value and type. In **statically typed** languages a variable's type cannot change after it has been declared. **Dynamically typed** languages, on the other hand, allow this by default. Both approaches have pros and cons. Dynamic typing is more forgivable and generally allows a programmer to code faster, but static typing offer higher performance and are less error-prone.

Sometimes a variable's value should not change in which case it is called a **constant**. Programming languages tend to write constants in capital casing.

### Declaring a Variable

Broadly speaking variables are declared using a **keyword** and an assignment of a value to a name. A keyword is a word reserved by the language for a specific purpose. `var` is a fairly common keyword used to declare variables.

We could write a template like so:
```
[KEYWORD] [NAME] = [VALUE]
```


When a variable name has more than one word we cannot use spaces. Instead, we can glue the words together and write the first character of every word after the first in uppercase. This style is called camel case, supposedly because of how the uppercase characters protrude from the text like humps on a camel's back:

```
var nameInCamelCase = ...
```

Another common style for variable names is snake case, which uses underscores between the words:
```
var name_in_snake_case = ...
```

---

Now that know about variables, let's make one. We can put the message with the special deal in a variable and name it `deal`:

```python
deal = "2 oranges for the price of 1!"
print(deal)
print(deal)
print(deal)
```

In other languages only the name of the command differs, some call it printing while others tell the computer more explicitly to write to the console:

JavaScript:
```javascript
let deal = "2 oranges for the price of 1!";
console.log(deal);
..
```
Rust:
```rust
let deal = "2 oranges for the price of 1!";
println!(deal);
..
```

C#:
```csharp
var deal = "2 oranges for the price of 1!";
Console.WriteLine(deal);
..
```

> Many programming languages end lines with a semicolon.

There is one more issue with the current code. We are telling the computer to print a message over and over. While three times is not that many, imagine if we want to make twenty calls or a hundred. That would look very messy. Once again, programming languages offer a solution: _loops_

---

## Repeating Actions with Loops

On many occasions programmers need to perform an operation a number of times. When this number is small we can choose to write it out manually but when a certain action must be done a lot of times that gets troublesome. To make life easier, programming languages provide **loops** to do things many times.

The most simple loop is the `while` loop. It keeps going while some condition holds. So if we want to do something twenty times we can declare a number variable and set it to `0`, then do whatever we want to do lots of times and with each round add `1` to the number, until it gets larger than the number of times we want to loop.

In Python code this looks like so:
```python
i = 0
while i < 20:
    print("One more time!")
    i++
```
Note that in programing we start counting from `0`. Also, `i` is the conventional name for an **iteration variable** as used in loops, and `i++` means _go to the next iteration_ by incrementing `i` by one. The program will print the text and increase `i` while it is smaller than `20`. Starting at `0` and ending at `19` that means twenty times in total.

We can put all sorts of conditions after the `while` keyword. One issue this can lead to is the creation of a loop that never stops because of a mistake made in the loop logic. When this occurs a program will likely freeze and crash. Let's look at code sample of an infinite loop, which also introduces a new data type: `booleans`, values that can be either `true` or `false`:

```python
on = true
while on:
    print("Looping..")
```
The code shows a variable `on` set to the value `true`. As long as this holds, the `while` loop will print text. However, there is nothing that sets `on` to `false` anywhere, meaning this loop will keep printing endlessly. Keep this phenomenon in mind when using `while`.

Aside from while loops there are `for` loops. Now here languages diverge somewhat in terms of style and syntax. First, let's look at the `for` loop in JavaScript, which in fact does the same as the Python `while` loop we made three paragraphs ago. Note that in the sample that follows `console.log` is the JavaScript equivalent of Python's `print` and `let` is a JavaScript keyword to declare a variable. 
```javascript
for (let i = 0; i < 20; i++) {
    console.log("One more time!");
}
```

<details>
The keyword "let" was chosen because programmers can then read variable declarations as "let my variable be this value", for example "let i be zero" or "let age be 21".
<summary>Why was "let" chosen as a keyword?</summary>

</details><br>

The code in the `for` loop means: 

* `let i = 0;` For a variable `i` starting at `0`
* `i < 20;` While `i` is smaller than `20`
* `i++` Incrementing `i` after every round of the loop
* `console.log("One more time!");` Log text to the console window

<!--"For a variable `i` starting at `0`, while `i` is smaller than `20`, incrementing `i` every round, `log` some text to the `console`. -->
Even though this is quite a mouthful the good thing is we can write it all on a single line.

In the C# language the loop looks nearly identical, can you spot the differences?
```csharp
for (int i = 0; i < 20; i++) {
    Console.WriteLine("One more time!");
}
```
Python and Rust on the other hand use `for .. in ..` syntax and create the numbers 0 to 20 in different ways:

```python
for i in range(20):
    print("One more time!)
```

```rust
for i in 0..20 {
    println!("One more time!");
}
```
The takeaway from the samples above is that all the `for` loop implementations share a **common part**. This idea of dividing concepts into a shared component at high-level and a specific implementation at low-level is a key part of computer programming.


---

Remember the store owner? He's still printing his deal of the day over and over. Let's build a loop so he can `print` his deals as many times as he likes. This is how the code looks right now:
```python
deal = "2 oranges for the price of 1!"
print(deal)
print(deal)
print(deal)
```

Let's assume the owner wants to print the deal a couple times extra. The new code uses a `for` loop to print 10 times:
```python
deal = "2 oranges for the price of 1!"
for i in range(10):
    print(deal)
```
This looks good. The message is printed ten times but we don't have to repeatedly write out the `print` call.

---

The store owner has different deals on Monday and Thursday. He wants to update the deal according to what day it is.

## Controlling Program Flow with Logic


```python
monday_deal = "2 oranges for the price of 1!"
thursday_deal = "Apples 30 percent off!"

day = "Monday"

for i in range(10):
    if day == "Monday":
        print(monday_deal)
    else:
        print(thursday_deal)
```

---

## Reusing Behavior with Functions

_A function performs a specific task with different inputs in multiple places._

Functions provide a means to reuse actions in multiple places. They are blocks of code that can take input, do something with it and return output. However, they can also take zero inputs and/or return no outputs at all. This is unlike mathematical functions which must have a unique output for every unique input.
A function's inputs are called **parameters** and function outputs are called **return** values.


In most high-level languages functions consist of a keyword, name, parameters and a function body enclosed in curly brackets. The keyword is specific to the language, for example `function`, `fn` or `def` (from `define`).

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
fn sum(a: i32, b: i32) -> i32 {
    a + b
}
```
There are only minor differences between these languages. Python uses a colon and indentation to signal a code block, whereas the other two use curly brackets. Rust does not need an explicit `return` statement and requires type annotations in the function parameters (in this case an `i`nteger that takes `32` bits of memory space. For more information see [Numbers](numbers.md)). 
