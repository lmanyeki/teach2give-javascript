# Operators  
These are symbols that perform operations on values.  
They are classified into the following categories:  
**Arithmetic operators**  
Used to perform mathematical operations.  
e.g.    let num1 =15;   
        let num2 = 5;  
        console.log(num1 + num2);  
For the **increment operator**, it can be used in two ways:  
- Post-increment (a++): returns the original value and then increments it.  
- Pre-increment (++a): increments first then returns the updated value.  
```
let x = 5;
console.log(x++); // 5 (returns first, then increments)
console.log(x); // 6

let y = 5;
console.log(++y); // 6 (increments first, then returns)
```
For the **decrement operator**, it can be used in two ways:  
- Post-decrement (a--): returns the original value, then decrements.  
- Pre-decrement (--a) – decrements first, then returns the updated value.  

|Operators|Description|Example|Result|
|-------|------|------|-------|
|+ |Addition| x=5+2| x=7|
|- |Subtraction| x=5-2 x=3|
|* |Multiplication| x=5*2 x=10|
|/ |Division |x=5/2 |x=2.5|
|% |Modulus (division remainder)| x=5%2 |x=1|
|++ |Increment |x=++5 |x=6|
|-- |Decrement |x=--5 |x=4|
|**|Exponentiation|x=5**5|x=3125|   


**Assignment operators**  
They are used to assign values to variables.  
They are categorised into the following:  
**Simple assignment operator (=)**  
Assigns a value to a variable.  
`let age=55;`
Given that x=10 and y=5, the table below explains the assignment operators:  
|Operator| Example| Same As| Result|
|-------|-------|-------|--------|
|= |x=10 ||x=10|
|+= |x+=y |z=x+y |z=15|
|-= |x-=y |z=x-y |z=5|
|*= |x*=y |z=x*y |z=50|
|/= |x/=y |z=x/y| z=2|
|%= |x%=y |z=x%y |z=0|
 
**Comparison**  
Used to compare values and return true or false.  
*Equality operator (==)*  
Returns true if left operand is equal to right operand and false if otherwise.  
This converts the data types of the variables; implicit conversion.  
```
let a = 10;
let b = 5;
console.log(a == b); // false
console.log(a == 10); // true
console.log(10 == "10"); // true
```
*Strict equality operator (===)*  
Returns true if left operand is equal to right operand and false if otherwise.  
The strict equality operator checks the data type as well, not just the values. This does not convert the data types of the variables.  
```
let a = 7;
let b = 3;
console.log(a === b); // false
console.log(a === 7); // true
console.log(10 === "10"); // false
```
*Not equal/inequality operator (!=)*  
Returns true if the operand on the left is not equal to the operand on the right and false if otherwise.  
```
let a = 10;
let b = 5;
console.log(a != b); // true
console.log(a != 10); // false

console.log(10 != "10"); // false
```
*Strict not equal to/Strict inequality operator (!==)*  
Returns true if the value on the left is not equal to the value on the right and false otherwise.  
It compares the data types of the operands.  
```
let a = 100;
let b = 50;
console.log(a !== b); // true
console.log(a !== 100); // false
console.log(100 !== "100"); // true
````
*Greater than (>)*  
This returns true if the operand on the left is greater than the operand on the right and false otherwise.  
```
let a = 15;
let b = 7;
console.log(a > b); // true
console.log(b > a); // false
```
*Less than (<)*  
This returns true if the operand on the left is less than the operand on the right and false otherwise.  
```
let a = 15;
let b = 7;
console.log(a < b); // false
console.log(b < a); // true
```  

*Greater than or equal to (>=)*  
This returns true if the operand on the left is greater than or equal to the operand on the right.  
```
let a = 15;
let b = 7;
console.log(a >= b); // true
console.log(b >= a); // false
console.log(10 >= 10); // true
```

*Less than or equal to (<=)*  
This returns true if the operand on the left is less than or equal to the operand on the right.  
```
let a = 10;
let b = 5;
console.log(a <= b); // false
console.log(b <= a); // true
console.log(10 <= 10); // true
```
**Logical**  
Used for boolean logic.   
*Logical AND operator (&&)* - Returns true if both operands are true.  
```
console.log(true && true); // true
console.log(true && false); // false
```
|Expression 1|Expression 2|Result|
|-------|-------|--------|
|true|true|true|
|true|false|false|
|false|true|false|
|false|false|false|

*Logical OR operator ()* - Returns true if at least one of the operands is true otherwise false.  
```
console.log(true || true); // true
console.log(true || false); // true
console.log(false || false); // false
```
|Expression 1|Expression 2|Result|
|--------|---------|------|
|true|true|true|
|true|false|true|
|false|true|true|
|false|false|false|

*Logical NOT operator (!) - Negates boolean value of an operator.  
```
console.log(!true); // false
console.log(!false); // true
```
 
**Bitwise**  
**Ternary**  
**Type**  



