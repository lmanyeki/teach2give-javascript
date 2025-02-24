# Functions

A function is a reusable block of code that perform a specific task, taking some form of input and returning an output.

They allow you to organize, reuse and modularize code.

It can take inputs, perform actions and return outputs; meaning, that they can be assigned to variables, passed as arguments, returned from other functions, stored in data structures and even created dynamically.

To define a function, you must use the **function** keyword, followed by a name, followed by parentheses ( ). Then you have to write the function logic between curly brackets { }.

Syntax:
```js
function functionName() {
  // function body
}
```
Example

```js
function sum(x, y) { 
    return x + y; 
}
console.log(sum(6, 9));
```
Output

`15`

### Return statement

In some situations, we want to return some values from a function after performing some operations. In such cases, we make use of the return. This is an optional statement. In the above function, “sum()” returns the sum of two as a result. 

### Function parameters

A parameter is a variable declared in a function definition and acts as a placeholder for the value that will be passed to the function when the function is being called.

In the above example, sum() takes two parameters, x and y.

An argument is the actual value passed to a function when it is called, it provides the data that the function or the method will operate on.

### Calling functions

After defining a function, the next step is to call them to make use of the function. 

We can call a function by using the function name separated by the value of parameters enclosed between the parenthesis.

Example

```js
// Function definition
function welcomeMsg(name) {
    return ("Hello " + name + " welcome to Murang'a University of Technology");
}

let nameVal = "Student";

// calling the function
console.log(welcomeMsg(nameVal));
```

Output

`Hello Student welcome to Murang'a University of Technology`

### Reasons for using functions

- Functions can be used multiple times, reducing redundancy.

- Break down complex problems into manageable pieces - modularity.

- Manage complexity by hiding implementation details.

- Can call themselves to solve problems recursively.

- Changes can be made in one place without affecting the entire codebase.

- Functions make code easier to understand.

### Choosing the right function type

- Use function declarations for regular reusable functions.

- Use arrow functions for concise, one-line functions.

- Use IIFE for code that runs immediately.

- Use callback functions for asynchronous operations like API calls.

- Use pure functions for predictable behavior without side effects.

### Function invocation

The function code you have written will be executed whenever it is called.

- Triggered by an event (e.g., a button click by a user).

- When explicitly called from JavaScript code.

- Automatically executed, such as in self-invoking functions.

### Function expression

It is similar to a function declaration without the function name. 

Function expressions can be stored in a variable assignment. 

Syntax:
```js
let studDetails= function(paramA, paramB) {
    // Set of statements
}
```

Example
```js
const mul = function (x, y) {
    return x * y;
};
console.log(mul(4, 5)); 
```
Output
`20`

## Types of functions

### Arrow functions

Arrow functions are a concise syntax for writing functions, introduced in ES6, and they do not bind their own this context.

Syntax:

`let function_name = (argument1, argument2 ,..) => expression`

Example
```js
const a = ["Hydrogen", "Helium", "Lithium", "Beryllium"];

const a2 = a.map(function (s) {
    return s.length;
});

console.log("Normal way ", a2);

const a3 = a.map((s) => s.length);

console.log("Using Arrow Function ", a3);
```
Output
```js
Normal way  [ 8, 6, 7, 9 ]
Using Arrow Function  [ 8, 6, 7, 9 ]
```
### Immediately Invoked Function Expression (IIFE)
IIFE functions are executed immediately after their definition. 

They are often used to create isolated scopes.

Example
```js
(function () {
    console.log("This runs immediately!");
})();
```
Output

`This runs immediately!`

### Callback functions

A callback function is passed as an argument to another function and is executed after the completion of that function.

Example
```js
function num(n, callback) {
    return callback(n);
}

const double = (n) => n * 2;

console.log(num(5, double));
```
Output

`10`

### Anonymous functions

Anonymous functions are functions without a name. They are often used as arguments to other functions.

Example
```js
setTimeout(function () {
    console.log("Anonymous function executed!");
}, 1000);
```

### Nested functions

Functions defined within other functions are called nested functions. 

They have access to the variables of their parent function.

Example
```js
function outerFun(a) {
    function innerFun(b) {
        return a + b;
    }
    return innerFun;
}

const addTen = outerFun(10);
console.log(addTen(5));
```
Output

`15`

### Pure Functions

Pure functions return the same output for the same inputs and do not produce side effects. 

They do not modify state outside their scope, such as modifying global variables, changing the state of objects passed as arguments or performing I/O operations.

Example
```js
function pureAdd(a, b) {
    return a + b;
}

console.log(pureAdd(2, 3));
```

Output

`5`
