# Coding with Basics

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

The **name** can be almost anything, although usually there are a few rules to follow and a couple of good practices to uphold. Programming is not like writing a novel, where you might pick words that are exceptionally beautiful, provocative or extravagant. When writing code we want to use names that are clear, concise and descriptive instead. This principle is often called _say what you mean_. This helps both yourself and your fellow developers in the present as well as the future.

**Types** are there so the computer understands how to operate on different data. For example, adding two numbers together is different than adding two text sentences together. Furthermore, types differ in how much memory space they take.

The **value** a variable can have is closely linked to its type. A numeric value might be `2` or `1991`. A text value might be `"Hello"` or `"2"`. Do you notice anything peculiar? The numbers are written down as is but the text is enclosed in quotes. That is because the numbers are of the _integer_ type while text is of type _string_.  
Why does this matter? Let's say we have a variable with the value `"2"`. Although it is a number, its type is not, and computers can only do calculations with numeric types. The value needs to change type which in programming is called **casting**. Some languages will automatically cast strings to integers in calculations but in others you will have to explicitly tell the program to do so.

Some languages require the programmer to specify the types of all variables. When this is the case the language is called **statically typed**. On the other hand, when type specification is not required, a language is called **dynamically typed**. Static typing has the advantage of catching errors early on, while dynamic typing is more forgivable and allows for faster coding.

### Declaring a Variable
Broadly speaking variables are declared with a **keyword** and _assign_ a value to a name. A keyword is reserved by a language for a specific purpose. A generic structure for a variable declaration looks like so:
```
[KEYWORD] [NAME] = [VALUE]
```
Not all languages use a keyword, with Python and Ruby as notable exceptions. `var` and `let` are fairly common keywords in the languages used in this course. The `=` symbol is the **operator** for assigning values to variables.

Names cannot have spaces in programming. Instead, software engineers use a few **conventions** to write multi-word variable names as well as clear and consistent code. The words are glued together and written with the first character of every word after the first in uppercase. This style is called _camel case_, supposedly because the uppercase characters protrude from the text somewhat like humps on a camel's back:
```python
nameInCamelCase
```

A different but very similar style is _pascal case_ where the first character is also uppercase:
```python
NameInPascalCase
```

Finally, another common style for variable names is _snake case_ which uses underscores between the words:
```python
name_in_snake_case
```

When a variable holds a value that should not change it is called a **constant**. Programming languages tend to write constants in capital case and with underscores for multiple words:
```python
CONSTANT_NAME
```

---

Now that know about variables, let's make one. We can put the message with the special deal in a variable and name it `deal`:

```python
deal = "2 oranges for the price of 1!"
print(deal)
print(deal)
print(deal)
```

In other languages only the name of the `print` command differs, some call it printing while others tell the computer more explicitly to write to the console. You will see that many programming languages end lines with a semicolon. Also, if you are wondering what the `.` stands for between the words in JavaScript and C#, it will be explained in [Using Arrays and Objects](arrays-and-objects.md). For now, just know that it does the same as `print` in Python:

JavaScript:
```javascript
let deal = "2 oranges for the price of 1!";
console.log(deal);
console.log(deal);
console.log(deal);
```
C#:
```csharp
var deal = "2 oranges for the price of 1!";
Console.WriteLine(deal);
Console.WriteLine(deal);
Console.WriteLine(deal);
```
Rust:
```rust
let deal = "2 oranges for the price of 1!";
println!(deal);
println!(deal);
println!(deal);
```

There is one more issue with the current code. We are telling the computer to print a message over and over. While three times is not that many, imagine if we wanted to make twenty calls or a hundred. That would look very messy. Once again, programming languages offer a solution: _loops_

---

## Repeating Actions with Loops

On many occasions programmers need to perform an operation a number of times. When this number is small we can choose to write it out manually but when a certain action must be done a lot of times that gets tedious. To make life easier, programming languages provide **loops** to do things many times.

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
on = True
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
Python and Rust on the other hand use `for .. in ..` syntax and create the number range in different ways:

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

The store owner has different deals on Monday and Thursday. He wants to update the deal according to what day it is. This brings us quickly to the next building block of code: _logic statements_.

## Controlling Program Flow with Logic
We can tune the flow of programs with the `if/else` construct. These statements use the keywords `if`, `else if` and `else` to guide actions based on certain conditions. The program evaluates these statements to either `true` or `false` using something called **boolean operators**. Because the equal sign `=` is used to assign values to variables the double equals `==` are used to check equality. In addition, the exclamation mark `!` can be used to check is something is _not_ true. It can be combined with the equality check into `!=` to check if two values are not equal.

Below is a sample `if` clause, written in Python. This code will print a birthday message if some variable `birthday` is `true`, and a different message otherwise:
```python
if birthday == true:
    print("Happy birthday to you!")
else:
    print("When's your birthday?")
```
And another sample, this time with an `elif` clause, the Python variant of `else if`. This code prints a different greeting based on the time of day stored in a variable `hour`. The example shows another boolean operator `&&` meaning _and_. In addition, it uses _less than_ and _greather than_ operators `<` and `>`:

```python
if hour < 12:
    print("Good morning.")
elif hour > 12 && hour < 18:
    print("Good afternoon.")
else:
    print("Good evening.")
```
Notice that in the final `else` statement, we don't need to check if it's evening anymore, because if the previous two checks did not pass, that means it is neither before twelve nor somewhere between twelve and six in the afternoon, meaning it has to be a time in the evening. If we had changed the `else` for `elif hour > 18`, the program would have performed that check, whereas the `else` is done in any case should the previous cases evaluate to false.

---

Back to the store, we are able to change the deal based on the day of the week. Python has pre-written code to deal with time but we have to import the code in our program before we can use it. This is unlike the `print` and `range` commands we saw earlier which are available by default.

The code we need is named `datetime` and it provides a means to get today's date with `today()`. After that we can format the date into only the day by calling `strftime()` which stand for `str`ing `f`ormat `time` and giving it a special input that correponds to the day of the week: `%A`.  
Phew, quite a lot of stuff right? We will look into some of these things in more detail later on. Have a look a the code below, and do not worry if the first two lines are not yet clear, just know that it allows us to get the day of the week so we can apply some logic.

```python
from datetime import datetime
day = datetime.today().strftime('%A')

monday_deal = "2 oranges for the price of 1!"
thursday_deal = "Apples 30 percent off!"

print("Welcome!")

for i in range(10):
    if day == "Monday":
        print(monday_deal)
    elif day == "Thursday":
        print(thursday_deal)
```
The program prints one deal on Monday and another on Thursday ten times after a welcome. This code uses a lot of concepts already! However, one thing still eludes, these commands like `print` and `range` that take a value and do something with it. They are called _functions_ and as it turns out, we can make our own.

---

## Reusing Behavior with Functions

Functions provide a means to reuse actions in multiple places. They are blocks of code that can take input, operate on it and return output. However, they can also take zero inputs and/or return no outputs at all.  
A function needs a **definition** where a list of **parameters** specifies the type of input it will take and the type of value it will **return**. Once defined, functions can be called by their name followed by parentheses where we can pass **arguments** to the call, which are the values for the parameters specific to that call only.  
How is a function defined? Most of the programming languages use a keyword, a name, zero or more parameters and a function body. The keyword is language-specific, for example `function`, `fn` or `def` (from `define`). Inside the function body most other building blocks of code can be used: variables, logic statements, loops and also calls to other functions. Do note that variables declared in a function are **local** to it, meaning they cannot be accessed by code outside the function. When a function completes these local variables are discarded.


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

---

The store owner wants to create another deal. On Fridays customers get 5% discount extra per  item of the same type. So:
- 1st item 5% discount
- 2nd item 10%
- 3rd item 15%
- ..

He wants the program to calculate the discount for him. He wants to fill in the number of items a customer buys and the item's price then get back the batch discount. We can use a function here which takes parameters for items and price and calculates the additional discount per item:
```python
def batch_discount(items, price):
    total_discount = 0
    for n in range(items):
        total_discount += (n + 1) * 0.05 * price
    
    return total_discount
```
This function does a lot of things, let's break them down:  
* `def batch_discount(items, price):` The function is defined with name `batch_discount` and parameters `items` and `price`
* `total discount = 0` We create a variable to store the discount and set it to an initial value `0`
* `for i in range(items):` The discount is increased per item bought. We use a loop to perform the discount calculation for each item.
* `total_discount += (n + 1) * 5 * price` The discount calculation for the _nth_ item. `+=` means we add to the current value of a variable and is short for `total_discount = total_discount + ..`. We need to use `n + 1` because the loop starts at `0` and then multiply that number with 5 because we apply 5% extra per item. Multiplied with the price of the item, we get the discount.

If we did this manually for 3 items at a price of 2 euros, the calculation would become:  

total_discount = `0`
 
total_discount += `(0 + 1) * 0.05 * 2 = 0.1` &rarr; `0 + 0.1 = 0.1`  
total_discount += `(1 + 1) * 0.05 * 2 = 0.2` &rarr; `0.1 + 0.2 = 0.3`  
total_discount += `(2 + 1) * 0.05 * 2 = 0.3` &rarr; `0.3 + 0.3 = 0.6`  

For `3` items the discount is `0.6` euros. And because we wrote a function, should a customer buy 20 oranges the store owner can fill in the price of an orange and 20 and get back the Friday discount from the program.

---

This rounds up the first parts of the course. If you followed along up to here, very well done! You learned four essential concepts of code from examples written in Python and gained some perspective on how those look in other kinds of languages. To remember what you learned it is important to practice. I recommend trying to write some lines of code where you make use of variables, loops, logic and functions in some way. Also see the [Language Setup Guide](setups.md) if you need to get started on that.

