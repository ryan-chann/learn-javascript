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
};

const sum = operate ((x, y) => x + y, 5, 3);
```

## 4. Best Practices for Writing Functions

### 4.1. Use Descriptive Names
Function names should clearly describe what the function does.
```
const fn = () => {...}; // Bad, What is fn??

const calculateSum = (a, b) => {...}; // Good
```

### 4.2. Keep Functions Small
Each function should perform a single task or responsibility.
```
// Bad, How should i know what processOrder does at a higher level view??
const processOrder(order) => {
    validateOrder(order);
    calculateTotal(order);
    applyDiscount(order);
    sendConfirmationEmail(order);
};

// Good
const validateOrder = (order) => {...};
const calculateTotal = (order) => {...};
const applyDiscount = (order) => {...};
const sendConfirmationEmail = (order) => {...};
```

### 4.3. Limit The Number of Parameter
If a function requires many parameter, <mark>consider using an object.</mark>
```
// Bad, Should I memorize all the arguments when I need to call the function??
const createUser = (name, age, email, address, phone) {...};

// Good
const createUser = (user) => {...};
```

### 4.4. Use Default Parameters
Provide default values for parameters to handle cases where arguments are not provided.
```
// Prone to error, especially if the invoker doesn't pass any arguments
const greet = (name) => {
    console.log('Hello, ${name}!`);
}

// Mitigate error with default parameters
const greet = (name = 'Guest') {
    console.log('Hello, ${name}!`);
}
```

### 4.5. Use Arrow Functions for Short Functions
Use arrow functions for simple functions to improve readability.
```
// Bad, Why use 3 lines for a single operation??
const add = (a, b) => {
    return a + b;
}

// Good
cost add = (a, b) => a + b;
```

### 4.6. Return Early
Handle special cases or error conditions at the beginning of a function to allow early exit of a function. This approach increases readability by reducing nesting.
```
// Without early return
const isAdult = (age) => {
    if (age >= 18) {
        return true;
    }
    else {
        return false;
    }
}

// With early return
const isAdult = (age) => {
    if (age < 18) {
        return false;
    }

    return true;
}
```