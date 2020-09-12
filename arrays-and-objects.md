# Using Lists and Objects

> In this guide you will learn how programming languages store and organize collections of data.

## Objects
_Objects_ are collections of data stored in **key-value pairs**. This means a value can be accessed by looking up its key. Object keys can be strings or numbers depending on the language and the implementation.

In general there are two ways to get a value from an object. The first is **index notation** where the name of the object variable is followed by the name of the key as a string enclosed in square brackets, for example `myObject["myKey"]`.  
The second form is called **dot notation** where the name of the object variable is followed by a dot `.` and the name of the key, for example `myObject.myKey`.

The following samples show how an object literal is declared and how the value `"John"` can be accessing the corresponding key `firstName`.

### Samples -  Object Declaration and Access

JavaScript
```javascript
let person = { 
    firstName: "John",
    lastName: "Smith" 
};

console.log(person["firstName"], person["lastName"]);
```

Python
```python
person = { 
    "firstName": "John",
    "lastName": "Smith" 
}

print(person["firstName"], person["lastName"])
```

C#
```csharp
var person = new { 
    firstName = "John",
    lastName = "Smith"
};

Console.WriteLine(person.firstName, person.lastName);
```

Rust
```rust
struct Person {
    firstName: &str,
    lastName: &str
}

let firstName = "John";
let lastName = "Smith";

let person = Person { firstName, lastName };

println!("{}, {}", person.firstName, person.lastName);
```

## Collections
Programming languages offer ways to store lists of values. They are types of objects so commonly used that most languages have them built-in. Across languages, four types of lists are often found:
* `Static arrays` hold a fixed number of elements of the _same_ type
* `Tuples` hold a fixed number of elements of _different_ types
* `Enums` are used to group values that are _related_ but _distinct_ from each other
* `Array lists`, also called `dynamic arrays` or `vectors` can hold a variable number of elements and types

Collections are indexed meaning each element has an **index** that can be used to access its value. Indexes are either integers or strings.

### Samples - Collections
A static array in C#:
```csharp
string[] names = {"Katie", "Bob", "Tony"};

Console.WriteLine(names[0]); // Writes "Katie" to the console.
```

A tuple in Python:
```python
prices_and_items = (10, "Book", 2, "Apple")

print(tupl[3])  # Prints "Apple".
```

An enum in Rust:
```rust
enum Seasons {
    Spring,
    Summer,
    Autumn,
    Winter,
}

println!("{?:}", Seasons::Summer);  // Pretty prints "Summer" (casting the enum variant to a string).
```

A dynamic array in JavaScript:
```javascript
let names = ["Katie", "Bob", "Tony"];

console.log(names[0]);  // Prints "Katie"
```


## Value Types versus Reference Types

An important thing to keep in mind when using different data types is how they are handled in computer memory and the way it affects their behavior. Programs store data from variables in two places. Primitive values such as integers and booleans are placed on the **stack**, which is somewhat like a stack of papers where each sheet holds the information about the value. When a new variable is declared it is added on top of the stack. When a value is no longer needed, it is taken out.  
On the other hand, complex types like arrays and objects are stored on the **heap**, while only a **pointer** to that location in memory is stored on the stack. This more indirect approach has the benefit of keeping the stack work fast. When a new variable is assigned the value of an existing object a new pointer or _reference_ is placed on the stack, pointing to the _same_ value on the heap.

```javascript
let firstObject = {
    luckyNumber: 7,
    randomNumber: 5
};

let secondObject = firstObject;

firstObject.luckyNumber = 3;
console.log(secondObject.luckyNumber);
```
Here we declare an object with two properties and then assign another variable to the object. Next, we change the value of the property `luckyNumber`.

What value is printed to the console for `secondObject.luckyNumber`?
* 7
* 3
* 5

