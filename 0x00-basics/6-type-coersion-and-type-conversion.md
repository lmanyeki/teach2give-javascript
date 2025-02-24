# Type Coersion and Type conversion  
### Type coersion  
The process of converting a value from one type to another. JavaScript coerces the type of one value to fit the type of the other value so that the operation can be carried out.  
```js
const sum = 35 + "hello"

console.log(sum)
// 35hello

console.log(typeof sum)
// string
```
In the above case, using the + sign with a number and a string, the number is coerced to a string, then the + sign is used for a concatenation operation.  
With the plus sign, it is more ideal for the number to be converted to a string (instead of the string converted to a number). This is because a number equivalent to a string is NaN but a string equivalent for a number, say 15, is "15" – so it makes more sense to concatenate two strings than to sum a number and NaN.  
In another example, we use times * for a number and a string. There's no operation with strings that involves multiplication, so here, the ideal coercion is from string to number (as numbers have compatible operations with multiplication). But since a string (in this case, "hello") is converted to a number (which is NaN) and that number is multiplied by 35, the final result is NaN.  
```js
const times = 35 * "hello"

console.log(times)
// NaN
```
```js
const string = ""
const number = 40
const boolean = true

console.log(!string)
// true - string is coerced to boolean `false`, then the NOT operator negates it

console.log(boolean + string)
// "true" - boolean is coerced to string "true", and concatenated with the empty string

console.log(40 + true)
// 41 - boolean is coerced to number 1, and summed with 40
```
### Type conversion  
You explicitly convert a value from one type to another.  
To explicitly convert types, you use the type **Constructors**. For example, to convert a number to a string:  
```js
const number = 30
const numberConvert = String(number)
console.log(numberConvert)
// "30"

console.log(typeof numberConvert)
// string
```
*Converting a number to a boolean:*  
```js
const number = 30

const numberConvert = Boolean(number)

console.log(numberConvert)
// true

console.log(typeof numberConvert)
// boolean
```
*Converting a boolean to a string:*  
```js
const boolean = false

const booleanConvert = String(boolean)

console.log(booleanConvert)
// "false"

console.log(typeof booleanConvert)
// string
```      



