# Data Types  
A data type is a type of value that can be identified by its value.  
The following are examples of data types in JavaScript:  
**String**  
A string is a series of letters and numbers enclosed in quotation marks ("") or single quotation marks ('') or backticks (``). JavaScript uses the string literally, it doesn't process it. You'll use strings for text you want displayed or values you want passed along.   
```js
let firstName = "Daniel";  
let middleName = 'Spectre';  
let lastName = `Oakland`;  
console.log(firstName, middleName, lastName); 
```  
**Number**  
It stores both integers and decimals.  
```js
let length = 25; // Integer
let weight = 69.9; // Decimal
let notANumber = NaN; // Not a Number (invalid math operation)
```
NaN - notANumber - A number that is not a legal number.  
The `Number.isNaN()` method returns true if the value is NaN and the type is a number.  
**Boolean**
It represents true or false and is used for decision making.  
```js
    let isKenyan = true;  
    let isUgandan = false; 
``` 
**Undefined**  
A variabe that has been declared and not initialised.  
```js
let novel;
console.log(nove;); // Output: undefined
```
**null**  
Intentional absence of a value.  
`let house = null; // No house yet` 
**BigInt**  
Used for numbers beyond JavaScript's Number. MAX_SAFE_INTEGER.  
let bigNumber = 12345678909876543234567823456789876n;  
*Don't use commas in numbers. Use underscores for js.*  
### Checking the type of variable  
You use the `typeof` operator.  
checking the typeof()  
console.log(typeof(firstName)); - This will output the type of data.  
```js
let bigNumber = 123456789012345678901234567890n;
console.log(typeof bigNumber); // bigint

const weight = 60;
const fullName = "Daniel Spectre";

console.log(typeof weight); // number
console.log(typeof fullName); // string
```