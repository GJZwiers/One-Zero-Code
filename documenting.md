# Writing Documentation
Coming Soon

Software code does not naturally speak for itself. Even the original writer's of pieces of code can have difficulty remembering the ins and outs after enough time has passed. Because of this reason it is vital to write both clear code and detailed documentation.

## Say What You Mean

Code can be written in ways that enhance readability. How variables and functions are named can have a large impact on the clarity of the code to a person who reads it for the first time. 

Compare the following code snippets, one a poorly worded function, the other clearly named.

```javascript
let whoAmI = "John";
```
```javascript
let name = "John";
```

When naming functions, take into account that some may only see its calls and not its definition. This holds true in particular when designing Application Programming Interfaces (APIs).

```javascript
function open(type) {

}
```

```javascript
function openFile(filetype) {

}
```
