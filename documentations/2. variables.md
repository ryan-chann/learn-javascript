# Variables
JavaScript variables are containers for storing data values. They allow you to store and manipulate information throughout your code.

## 1. Declaration
Variables can be declared with three keywords.

### `var`
Variables declared with the `var` keyword has <mark>global scope</mark> and is one of the oldest way to declare variables. This is <mark>not recommended except when working on legacy browsers.</mark>
```
var placeholder
```

### `let`
Variables declared with the `let` keyword has <mark>block scope</mark> and it is more preferable.
```
let placeholder
```

### `const`
Variables declared with the `const` keyword also has <mark>block scope</mark> but the values of it cannot be reassigned after it has been initialized. This is also more preferable.
```
const placeholder
```
The `const` keyword creates a constant reference but not a constant value which means that primitive types like number and strings, the value cannot be changed. However the contents of an object can still be modified.

> **Note:** Always use `const` and `var` to declare variables.


## 2. Scope
### 2.1. Global Scope
Globally scoped variables are declared outside a function or using the `var` keyword, which can be accessed in anywhere.
```
let globallyScopedVariable

function = () => {
    globallyScopedVariable = "Value"; // No Error
}
```

### 2.2. Function Scope
Functionally scoped variables are declared inside a function and can be accessed only in that function.
```
function = () => {
    const functionallyScopedVariable = "Value";
}

functionallyScopedVariable = "NewValue"; // Error
```
### 2.3. Block Scope
Block scoped variables are declared inside a scope and can be access only within the curly braces `{}`.
```
function = () = {
    if (...) {
        const blockScopedVariable = "Value";
    }
    else {
        blockScopedVariable = "NewValue"; // Error
    }
}
```

## 3. Hoisting
Hoisting is JavaScript's default behavior of moving declarations to the top of the current scope. However, only the declarations are hoisted, not the initializations.
```
let hoistedVariable;

function = () => {
    hoistedVariable = "Initialized"
}
```
The above example shows how variables can be hoisted by declaring variables without initilization on top of the code. The initialization is performed in the codes below.

## 4. Javascript Naming Conventions
<table>
<tr>
    <th>Naming Convention</th>
    <th>Usage</th>
</tr>
<tr>
    <td>camelCase</td>
    <td>Variables, Functions</td>
</tr>
<tr>
    <td>PascalCase</td>
    <td>Classes, Interfaces</td>
</tr>
<tr>
    <td>UPPERCASE</td>
    <td>Constants</td>
</tr>
<tr>
    <td>snake_case</td>
    <td>Database names, APIs</td>
</tr>
<tr>
    <td>kebab-case</td>
    <td>URLs, CSS properties</td>
</tr>
</table>

## 5. Best Practices for Naming Variables
The purpose of high-level programming languages is to ease developers in writing programs through english-like codes. Writing human-readable codes can be achieved with good variable names.
### 1. Be Descriptive
Use meaningful and descriptive names that convey the purpose of the variable
```
let x = 10; // Bad, What is x??

let userAge = 10; //Good
```

### 2. Avoid Abbreviation
Avoid using abbreviations or single letters unless they are well-known such as `i` for loop index.
```
let fn = "John"; // Bad, What is fn??

let firstName = "John" // Good
```

### 3. Use Contextual Names
Use names that provide context and make the code self-explanatory.
```
let date = newDate(); // Bad, what date is this?

let currentDate = new Date(); // Good
```
