# Rest operator

This allows functions to accept an indefinite number of arguments as an array. It collects multiple arguments into a single array parameter.
```js
// Rest Parameter
function myFunc(...args) {
    console.log(args);
}
myFunc(1, 2, 3, 4, 5);
```
Output

`[ 1, 2, 3, 4, 5 ]`

The …args in myFunc(…args) collects all passed arguments into an array called args.

When calling myFunc(1, 2, 3, 4, 5), it prints [1, 2, 3, 4, 5] because all arguments are grouped into args.

### Using rest parameter in functions

The rest parameter allows a function to accept an indefinite number of arguments as an array.
```js
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}
console.log(sum(1,2,3,4,5))
```
Output

`15`

The sum function uses the rest parameter to gather arguments. 

It calculates the sum of all passed numbers.

…numbers gathers all arguments into an array.

The reduce method iterates over the array and sums the values.

The default value of 0 ensures the sum starts correctly.

numbers would become an array after passing of arguments to the sum function and it will look like [1,2,3,4,5].
### Use cases of rest parameter

### Collecting function arguments

The rest parameter collects names into an array. The function greets all the names.
```js
function greet(greeting, ...names) {
    return `${greeting}, ${names.join(' and ')}`;
}
console.log(greet("Pranjal", "Tanamaya", "Sonam"));
```
Output

`Pranjal, Tanamaya and Sonam`

…names gathers remaining arguments.

The join method creates a string combining names.

The result is a personalized greeting.

### Filtering properties in objects

Destructuring extracts property a. The rest parameter gathers remaining properties.
```js
const { a, ...rest } = { a: 1, b: 2, c: 3 };
console.log(a)
console.log(rest)
```
Output
```
1
{ b: 2, c: 3 }
```
a is assigned 1.

…rest collects { b: 2, c: 3 }.

This separates key-value pairs.

### Destructuring with rest

Destructuring extracts the first element. The rest parameter gathers remaining elements.
```js
const [first, ...rest] = [1, 2, 3, 4];
console.log(first)
console.log(rest)
```
Output
```
1
[ 2, 3, 4 ]
```
first receives the value 1.

…rest collects [2, 3, 4].

Both variables are distinct.

### Function default parameters

The rest parameter collects numbers. The function multiplies each by a given factor.
```js
function mul(factor, ...nums) {
    return nums.map(num => num * factor);
}
console.log(mul(2,1,2,3,4,5))
```
Output

`[ 2, 4, 6, 8, 10 ]`

…numbers gathers extra arguments into an array.

map applies the multiplication to each element.

The result is a new array of products.