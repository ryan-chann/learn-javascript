# Comments
Comments in JavaScript are used to add explanations, notes, or disable code without affecting its execution. They are essential for improving code readability and maintainability.

## 1. Types of comments
### 1.1. Single-line comments
```
// This is a single-line comment
```
Place `//` before a line of code, single-line comments can be used to <mark>disable a particular line of code</mark> or <mark>mark areas that needs improvement</mark>

### 1.2. Multi-line comments
```
/*
    This is a multi-line comment.
    Multi-line comments are also known as block comments.
*/
```
Cover a block of code with `/*` and `*/`, multi-line comments can be used to <mark>disable a block of code</mark>, <mark>write TODO notes</mark>, or <mark>explain complex logic or algorithms</mark>.

### 1.3. JSDoc comments
```
/**
 * @param {number} length - The length of the rectangle.
 * @param {number} width - The width of the rectangle.
 * @returns {number} The area of the rectangle.
*/

```
Cover a block of code with `/**` and `*/`, JSDoc comments can be used to aid <mark>automatic documentation generation</mark>, <mark>enhance code readability</mark>, and <mark>improve code quality</mark>. JSDoc support numbers of annotation for different types of data.
### 2. JSDoc Annotation

#### 2.1. `@Param`
Describe the parameter values of a function

Syntax:
```
/**
    * @param{type} name - description
*/
```

Example:
```
/**
    * @param{String} firstName - User first name
    * @param{String} lastName - User last name
*/
```

#### 2.2. `@Returns` / `@Return`
Describe the return value of a function

Syntax:
```
/**
    * @returns {type} - description
*/
```
Example:
```
/**
    * @returns {String} - Full Name
*/
```

#### 2.3. `@type`
Explicitly define variable type with comments to increase readability, commonly used in conjunction with variables.

Syntax:
```
/**
    * @type {type}
*/
```
Example:
```
/**
    * @type {String}
*/
let fullName;
```

#### 2.4. `@typedef`
Refers to *Type Definition*, commonly used to define user-defined data types like objects and used in conjunction with the `@property` annotation

Syntax:
```
/**
    * @typedef {type} typeName
*/
```

Example:
```
/**
    * @typedef {Object} User
    * @property {string} id - User's unique identifier
    * @property {string} name - User's name
    * @property {string} email - User's email address
    * @property {number} age - User's age
*/
```

#### 2.5. `@property`
Describe the properties of an object type, commonly used in conjuction with the `@typedef` annotation

Syntax:
```
/**
    * @property {type} propertyName - Description
*/
```

Example:
```
/**
    * @typedef {Object} User
    * @property {string} id - User's unique identifier
    * @property {string} name - User's name
    * @property {string} email - User's email address
    * @property {number} age - User's age
*/
```

See more JSDocs annotation at [Official JSDoc Documentation](https://jsdoc.app/)