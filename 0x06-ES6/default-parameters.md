# Default parameters

Function parameters with default values are initialized with default values if they contain no value or are undefined. 

It may be useful to set a different default value. 

Syntax
```js
function name(parameter=value,...parameters) {

}
```

Example
```js
function multiply(a, b) { 
    return a * b; 
} 
  
let num1 = multiply(5); 
console.log(num1); 
let num2 = multiply(5, 8); 
console.log(num2);
```
Output:
```js
NaN
40
```
Example  
```js
function multiply(a, b = 2) { 
    return a * b; 
} 
  
let num1 = multiply(5); 
console.log(num1); 
let num2 = multiply(5, 8); 
console.log(num2);
```
Output:
```
10
40
```
