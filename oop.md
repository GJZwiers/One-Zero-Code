# Object-Oriented Programming

> In this guide you will learn how to organize application parts through an abstraction called classes.

As programs grow, developers need ways to structure and organize the relationships and interactions between application components. One way of doing so is called **object-oriented programming** (OOP), where related data and behavior are wrapped in **classes**.

_Classes_ are objects with blueprints for variables and functions that work together. Once defined, a programmer can create multiple **instances** of a class where each instance can be in a different state. This means that while each instance is made from the same blueprint, it can have its own values for the data at any given time.

## Terminology
Variables defined inside classes are called **fields**, while functions in classes are called **methods**.  Some fields have additional logic involved in assigning and retrieving their values, in which case they are called **properties** that use a **getter** and/or a **setter** method. However, the terms _field_ and _property_ are often used loosely.  

Instead of a variable keyword, class fields are prefixed with one or more **modifiers**. For example, many languages use a **readonly modifier** to mark a field's value as constant. In addition, fields and methods can be prefixed with an **access modifier**. This attribute determines what parts of the application have access. **Public** means a field or method can be accessed by anything inside or outside the class. **Private** means only the class itself has access, while **protected** means the class as well as other classes that extend from it have access (for more information on protected access see [Inheritance](interactions.md)). More access modifiers exist in certain languages but the three mentioned here are used most often.

Classes use a special **constructor** method to make new instances. This method sits on the **static side** of a class meaning it can called on the class itself. A programmer can define additional methods on the static side using the **static modifier**. All other methods sit on the **instance side** and can only be called on instances of the class made with the constructor.

Instances have a way to refer to themselves, which is needed to differentiate between multiple instances. This is done using a self-referencing keyword, generally named **this** or **self** in the programming language.


## Class Design
Classes tend to have a public side which exposes the results of their private or internal operations.



### Samples - Defining a Class

TypeScript
```typescript
class Calculator {

}
```

Python
```python
class Calculator:
    pass
```

C#
```csharp
public class Calculator {

}
```

Rust*
```rust
struct Calculator {

}

impl Calculator {

}
```
##### * In the Rust language classes are split into `struct`ures and `impl`ementations. This has to do with advanced OOP topics which you can read more about in [Interchangeable Parts](interchangeable-parts.md).

## Initialization
An instance of a class is initialized with a special method called a **constructor**. This method can take input parameters that are used to set the starting state of that instance.

TypeScript
```typescript
class Calculator {

    constructor() {

    }
}
```

Python
```python
class Calculator:

    __init__():
        pass
```

C#
```csharp
public class Calculator {

    public Calculator() {

    }
}
```

Rust*
```rust
struct Calculator {

}

impl Calculator {
    pub fn new() -> Calculator {
        
    }
}
```


## Self-Reference



## 