# DAY 2
## Getting Started with ES2015
## Creating Functions with Arrow Syntax

A function has been created in one of two ways:
* A function declaration
* A function expression

A function declaration begins with the keyword 'function' followed by the identifier.

A function expression begins with the variable type (let, var, const), and ends with a semicolon.

Introduced to ECMAScript 2015 is the arrow function. It is similar to a function expression except that it gets rid of the 'function' keyword and includes a '=>' symbol.

```javascript
const sayName = (parameters) => {
    const message = "My name is " + name;
    console.log(message);
}
```

If your arrow function only takes in one argument, then you don't need to include parenthesis. However, you need parenthesis if your function has zero or more than one parameters.
You can also remove the curly braces when there is one line of code in your function.

```javascript
const square = x => return x * x;

const multiply = (x, y) => return x * y;
```