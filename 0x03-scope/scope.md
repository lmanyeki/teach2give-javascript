# Scope

Scope in JavaScript determines the accessibility of variables and functions at various parts of one’s code or program.

Scope helps us to determine a given part of a code or a program, what variables or functions one can access and what variables or functions one cannot access.

The following are the types of scope: 

### Global Scope

Variables or functions that are declared under a global namespace (like area or location) are referred to as **global scope**. 

It means that all the variables that have global scope can be easily accessed from anywhere within the code or a program.

Example
```
// Global scoped letiable
let global_letiable = "Software development class";
 
// First function...
function first_function() {
    return global_letiable;
}
 
// Second function...
function second_function() {
    return first_function();
}
 
console.log(second_function());
```

Output

`Software development class`

### Local or Function scope

These are variables that are declared inside a function or a method.

It means those variables or functions which are declared inside the function or a method can be accessed within that function only.

Example
```
function main_function() {
 
    // letiable with local scope...    
    let a = 2;
 
    // Nested function having function scope    
    let multiply = function () {
 
        // It can be accessed and altered as well
        console.log(a * 5);
    }
 
    // Will be called out when main_function gets called
    multiply();
}
 
// Displays the result...
console.log(main_function());
 
// Throws a reference error since it 
// is a locally scoped letiable
console.log(a);
 
// Throws a reference error since it 
// is a locally scoped function
multiplyBy2();
```

Output
```
10
undefined
Uncaught ReferenceError: a is not defined
```
## Block scope

Block scope is related to the variables or functions which are declared using let and const since var does not have block scope.

This scope tells us that variables that are declared inside a block { }, can be accessed within that block only, not outside of that block.

Example
```
{
    let x = 13;
}
// Throws a reference error 
// since x is declared inside a block which 
// cannot be used outside the block
console.log(x);
```
Output

`Uncaught ReferenceError: x is not defined`

### Lexical scope

Lexical scope is the scope of a variable or function determined at compile time by its physical location in the code. 

Unlike dynamic scope, which depends on how functions are called at runtime, lexical scope is static and remains the same throughout the program’s execution.

### Importance of scoping variables appropriately

- Improve code readability and avoid unintended side effects.

- Prevent naming conflicts.

### Scope chain

JavaScript engine uses scopes to find out the exact location or accessibility of variables and that particular process is known as **scope chain**.

Scope chain means that one variable has a scope and is used by another variable or function having another scope.

This complete chain formation goes on and stops when the user wishes to stop it according to the requirement.

Example
```
// Global letiable
let global_letiable = 20;
 
function main_function() {
    // Local letiable
    let local_letiable = 30;
 
    let nested_function = function () {
 
        // Display the value inside the local letiable
        console.log(local_letiable);
    }
 
    let another_nested_function = function () {
 
        // Displays the value inside the global letiable
        console.log(global_letiable);
    }
 
    nested_function();
    another_nested_function();
}
 
main_function();
```
Output
```
30
20
```
