# High order array methods

### array join() method

This creates and returns a new string by concatenating all elements of an array. It uses a specified separator between each element in the resulting string.
```js
let a = ["food", "soda", "dessert", "juice"];
console.log(a.join('|'));
```
Output

`food|soda|dessert|juice`

### array delete operator

The delete operator is used to delete the given value which can be an object, array or anything.
```js
let emp = { 
    firstName: "Riya", 
    lastName: "Kaur", 
    salary: 40000
} 

console.log(delete emp.salary); 
console.log(emp);
```
Output
```js
true
{ firstName: 'Riya', lastName: 'Kaur' }
```

### array concat() method
The concat() method is used to concatenate two or more arrays and it gives the merged array.
```js
let a1 = [11, 12, 13];
let a2 = [14, 15, 16];
let a3 = [17, 18, 19];

let newArr = a1.concat(a2, a3);
console.log(newArr);
```
Output
```js
[
  11, 12, 13, 14, 15,
  16, 17, 18, 19
]
```

### array flat() method

The flat() method is used to flatten the array i.e. it merges all the given array and reduces all the nesting present in it.
```js
const a1 = [['1', '2'], ['3', '4', '5',['6'], '7']];
const a2 = a1.flat(Infinity);
console.log(a2);
```
Output
```js
[
  '1', '2', '3',
  '4', '5', '6',
  '7'
]
```

### array.slice() method

The slice() method returns a new array containing a portion of the original array, based on the start and end index provided as arguments
```js
const a = [1, 2, 3, 4, 5];
const res = a.slice(1, 4);
console.log(res); 
console.log(a)
```
Output
```js
[ 2, 3, 4 ]
[ 1, 2, 3, 4, 5 ]
```

### array some() method

The some() method checks whether at least one of the elements of the array satisfies the condition checked by the argument function.
```js
const a = [1, 2, 3, 4, 5];
let res = a.some((val) => val > 4);
console.log(res); 
```
Output

`true`

### array map() method
The map() method creates an array by calling a specific function on each element present in the parent array. It is a non-mutating method.
```js
let a = [4, 9, 16, 25];
let sub = a.map(geeks);

function geeks() {
    return a.map(Math.sqrt);
}
console.log(sub);
```
Output

`[ [ 2, 3, 4, 5 ], [ 2, 3, 4, 5 ], [ 2, 3, 4, 5 ], [ 2, 3, 4, 5 ] ]`

### array filter() method
The filter() method creates a new array with all elements that pass the test implemented by the provided function. It does not modify the original array.
```js
let a1 = [1, 2, 3, 4, 5]
let a2 = a1.filter((num) => num > 1)
console.log(a2)
```
Output

`[ 2, 3, 4, 5 ]`

### array reduce() method

The reduce() method is used to reduce the array to a single value and executes a provided function for each value of the array (from left to right) and the return value of the function is stored in an accumulator.
```js
let a = [88, 50, 25, 10];
let sub = a.reduce(geeks);

function geeks(tot, num) {
    return tot - num;
}
console.log(sub);
```

Output

`3`

### array reverse() method

The reverse() method is used to reverse the order of elements in an array. It modifies the array in place and returns a reference to the same array with the reversed order.
```js
let a = [1, 2, 3, 4, 5];
a.reverse();
console.log(a);
```
Output

`[ 5, 4, 3, 2, 1 ]`

### Array values() method
The values() method returns a new Array iterator object that contains the values for each index in the array.
```js
const a = ["Apple", "Banana", "Cherry"];
const res = a.values();

for (const value of res) {
    console.log(value);
}
```
Output
```js
Apple
Banana
Cherry
```

### array find()

The `find()` method returns the value of the first element in the array that satisfies the provided testing function. Otherwise, it returns undefined.

Does not return new but returns the found number instead:
```js
const numbers = [1, 2, 3, 4];
const found = numbers.find((num) => num === 3);
console.log(found);
```
Output

`3`

### array findIndex

Returns the index of the first element that matches a condition.
```js
const numbers = [10, 20, 30, 40, 50];

const index = numbers.findIndex((num) => num > 25);
console.log(index);
```
Output

`2`

### array some

Checks if at least one element passes a condition.

If so, it returns true, otherwise, it returns false.
```js
const numbers = [1, 3, 5, 7];

const hasEven = numbers.some((num) => num % 2 === 0);
console.log(hasEven);
```
Output

`false`

### array every

Checks if all elements in an array pass a condition.

If so, it returns true, otherwise it returns false.
```js
const numbers = [2, 4, 6, 8];

const allEven = numbers.every((num) => num % 2 === 0);
console.log(allEven);
```
Output

`true`