# DAY 1
## Getting Started with ES2015
## Let and Const

const - should be your first choice when declaring variables. const is used to store values that shouldn't change.

You'll want to use constants when getting elements from a page, or when storing functions into variables. Do not use const when the value will change.

adding const before a variable inside a function will keep that variable scoped only to that function.

BEFORE:

variable 'name' with value 'Andrew' will be overwritten by the createFullName function. 'name' will now be set to 'Joel Kraft'.

```javascript
var name = "Andrew";
      
      function createFullName(fName, lName) {
          name = fName + " " + lName;
          console.log(name);
      }
      console.log(name);
      createFullName("Joel", "Kraft");
```
AFTER:

variable 'name' will keep the value 'Andrew' because it is a constant. 'const name' inside the createFullName function will only be scoped to that function.



```javascript
const name = "Andrew";
      
      function createFullName(fName, lName) {
          const name = fName + " " + lName;
          console.log(name);
      }
      console.log(name);
      createFullName("Joel", "Kraft");
```
Const does not prevent arrays and objects from being modified. Using methods such as .push() or adding an object property will change a constant value. const aims to prevent a value from being reassigned completely. Const cannot be initialized with an empty value;

let - let allows variables to be reassigned values, like the var keyword. You should use let when you're...
* incrementing an index in a loop
* adding strings together

### In summary...
* From now on, do not use the var keyword. Use let and const.
* Const should be the first choice to use when declaring a variable

## Template Literals
Template literals - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals

Writing template literals is the same as creating string literals, except instead of single / double quotes, you enclose strings with back ticks.

They are very helpful with creating multiline strings.

BEFORE: 

```javascript
const vegetableList =
"<ul>" +
    "<li>Potato</li>" +
    "<li>Onion</li>" +
    "<li>Broccoli</li>" +
  "</ul>";
```

AFTER:


The use of template literals removes the need for double quotes and concatenation using '+' operator.

```javascript
const vegetableList = 
  `<ul>
    <li>Potato</li>
    <li>Onion</li>
    <li>Broccoli</li>
  </ul>`;
```
  Interpolation - the use of placeholders inside strings to be interpreted later. Template literals allow javascript to interpolate.

  ```javascript
    ${`    `}
  ```
The dollar sign and brackets are used to mark the dynamic values in the template literal.

You can include function expressions in template literals.