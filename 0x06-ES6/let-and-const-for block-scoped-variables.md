# let and const for block scoped variables

The let & const keyword facilitates the variables to be block scoped. 

In order to access the variables of that specific block, we need to create an object for it. 

Variables declared with the var keyword, do not have block scope.

- let - Variables declared using the ‘let’ keyword are similar to variables declared using the ‘var’ keyword with just one difference. 

Variables declared using ‘let’ will have block scope and will not get hoisted to the starting of the function. 

So, if we try to access those variables outside their block scope, we’ll get a reference error saying the variable is not defined.
```js
function printIfGFG( text){
   if(text=="GeeksforGeeks"|| text=="GFG") {
   let message = "Verified Geek";
   console.log(message); // Output: Verified Geek
    }
console.log(message); // Output: Uncaught ReferenceError: message is not defined
}
printIfGFG("GFG");
```
Also, variables declared with the “let” keyword can be redefined but not redeclared.
```js
let msg = "Try again";
msg = "Try again later"; // Output: Try again later
```
```js
let msg = "Try again";
let msg = "Try again later"; // Output: Uncaught SyntaxError: 
Identifier 'msg' has already been declared
```
- const - Variables declared using the “Const” keyword are similar to variables declared using the “let” keyword with an additional feature that once declared and defined, their value cannot be changed.

The primary use of `const` variables is to make read-only constants like
```js
const PI = 3.14
const MAX_USERS = 1000;
```
Also, it is compulsory to define const variables at the time of declaration itself.
```js
const pi; // Syntax Error
pi = 3.14
```

### Hoisting

Hoisting refers to the behaviour where JavaScript moves the declarations of variables, functions and classes to the top of their scope during the compilation phase. 

This can sometimes lead to surprising results, especially when using var, let, const, or function expressions.

- Hoisting applies to variable and function declarations.

- Initializations are not hoisted, they are only declarations.

- ‘var’ variables are hoisted with undefined, while ‘let’ and ‘const’ are hoisted but remain in the Temporal Dead Zone until initialized.