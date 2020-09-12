# Interchanging Parts with Object Interfaces

> In this guide you will learn what object interfaces are and how they can make program code more flexible. Basic knowledge of classes and object-oriented programming is assumed. 

Object **interfaces** are contracts. When classes **implement** an interface they agree to have a certain _shape_, meaning they need to have the attributes defined in the interface. Think of a coffee machine with pads where it is possible to change brands easily because each coffee pad fits in the holder. Using interfaces allows developers to switch to a different implementation for some application component without changing existing code.

Imagine a program that calculates a person's monthly financial balance from a bank statement and shows its outputs to the user. During early development, a simple solution may be enough where the results are logged to the console. Later however, we may want to log to a text file or an online dashboard.

How would we go about writing this code? First, let's do it without using interfaces, to see where they might come in handy. We start by writing two classes, one to do the logging and one to calculate the balance. Note that for simplicity the balance sheet and the results in the example are set to plain strings.

```typescript
class Logger {
    log(text) {
        console.log(text);
    }
}

class BalanceCalculator {
    private balance: string;
    private logger: Logger;

    constructor(balance: string, logger: Logger) {
        this.balance = balance;
        this.logger = logger;
    }

    calculateBalance() {
        let summary = "total income: 2000; total expense: 1500; balance: 500";
        this.logger.log(summary);
    }
}
```
The reason for placing the `log` method in its own class is to make this feature reusable in other parts of the code. We could have written it as a `function` instead if there was no requirement to add more detail to the logging behavior in the future.  
Now what if we want to change the way the balance is logged? We could just rewrite `log` with a new implementation. However, if more parts of the application made use of it, that would force all of them to use the same thing. Though perhaps that is not desired and we want the `BalanceCalculator` to have more complex logging but more simpler solutions in other parts of the code.  
This is where interfaces come to the rescue. We can define one for classes that log, then implement it on the `Logger` class. Finally, we change the constructor of the `BalanceCalculator` class to no longer take the hard-coupled `Logger`, but a more loosely coupled interface that has the ability to log something. 


```typescript
interface Logs {
    log: (text: string) => void;
}

class Logger implements Logs {
    log(text: string): void {
        console.log(text);
    }
}

class BalanceCalculator {
    private balance: string;
    private logger: Logs;

    constructor(balance: string, logger: Logs) {
        this.balance = balance;
        this.logger = logger;
    }

    calculateBalance() {
        let summary = "total income: 2000; total expense: 1500; balance: 500";
        this.logger.log(summary);
    }
}
```
A lot is going on here at once, so let's go over the pieces one at a time:

```typescript
interface Logs {
    log: (text: string) => void;
}
```
First we declare an interface with its identical keyword and give it a name. Then we define the attributes that any implementing class needs to have, in this case a method named `log` that takes one parameter `text` of type `string` and returns type `void`, meaning nothing (see [Functions](programming.md#functions) if any of these concepts are not familiar).

```typescript
class Logger implements Logs {
    log(text: string): void {
        console.log(text);
    }
}
```
Next, we update the `Logger` class to implement the new interface. Note that if we removed the `log` method at this point we would get some error saying the `Logs` interface is not properly implemented.

```typescript
class BalanceCalculator {
    private balance: string;
    private logger: Logs; <--

    constructor(balance: string, logger: Logs) { <--
        this.balance = balance;
        this.logger = logger;
    }

    calculateBalance() {
        let summary = "total income: 2000; total expense: 1500; balance: 500";
        this.logger.log(summary);
    }
}
```
In the `BalanceCalculator` we have changed the `logger` field to take the `Logs` interface type instead of the `Logger` class type. This means that any class upholding the interface can be passed as a constructor parameter.

Now, if at some point we design a new way to log the summary from `BalanceCalculator` we can simply write another class that implements `Logs`. The code we wrote already will be untouched, meaning other classes that also make use of `Logger` will be unaffected by the change.







```typescript
let balance = "some list of transactions";
let logger = new Logger();
let calculator = new BalanceCalculator(balance, logger);

calculator.calculateBalance();
```



```typescript
interface Logs {
    (output: string): void
}
```

```csharp
interface ILog {
    void Log(string output);
}
```
