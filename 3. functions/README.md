# Functions
JavaScript functions are fundamental building blocks in programming. They allow you to encapsulate <mark>reusable code</mark>, making your programs more organized and efficient.

## 1. Declaration
### 1.1. Function Declaration
The traditional way to define a function.

Syntax:
```
function name(parameter) {
    // Implementation
}
```
<br>

Example:
```
function greet(name) {
    return `Hello, $(name)!`;
}
```

### 1.2. Function Expression
Assigning a function to a variable, which means that the <mark>variable is a function object.</mark>

Syntax:
```
const placeholder = function(parameter) {
    // Implementation
}
```
<br>

Example:
```
const greet = function(name) {
    return `Hello, $(name)!`;
}
```

### 1.3. Arrow Function
Brief way to write function expression.

Syntax:
```
const placeholder = (parameter) => {
    // Implementation
}

// Write simple function without curly braces to directly return the value
const greet = (parameter) => // Implementation
```
<br>

Example:
```
const greet = (name) => {
    return `Hello, ${name}!`;
}

const greet = (name) => `Hello, ${name}!`;
```

<br>

> **Note:** Functions can return a value using the `return` keyword. If no return statement are used, the function returns `undefined`.

## 2. Parameter & Arguments
Every functions can accept parameters, which are placeholders for values that will be passed when the function is called. The actual value passed are called arguments
```
const sum = (a, b) => return a + b; // a & b are parameters

console.log(sum(4, 5)); // 4 & 5 are arguments
```

## 3. Higher-Order Functions
In JavaScript, <mark>functions can be passed as arguments to other functions or returned from functions</mark>, making them higher-order functions.

```
const operate = (functionArgument, a, b) => {
    return functionArgument(a, b);
}

const sum = operate ((x, y) => x + y, 5, 3);
```