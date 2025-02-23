# Arrays

An array is a collection of elements stored at contiguous memory locations.

An array is a special variable, which can hold more than one value.

Each value is called an element, and each element has a numeric position in the array, known as its index.

They are zero-indexed, meaning the first element is at index 0, the second at index 1, and so on.

## Creating an array

### Array literal

Creating an array using array literal involves using square brackets [] to define and initialize the array.

Syntax:

`const arrayName = [item1, item2, item3, ...];`

Example

```js
// Creating an Empty Array
let a = [];
console.log(a);

// Creating an Array and Initializing with Values
let b = [10, 20, 30];
console.log(b);
```

Output

```
[]
[ 10, 20, 30 ]
```

### Create using new keyword (Constructor)

The “Array Constructor” refers to a method of creating arrays by invoking the Array constructor function.

Syntax:

`const arrayName = new Array(item1, item2, item3, ...)`

Example

```js
// Creating and initializing an array with values
let a = new Array(10, 20, 30);

console.log(a);
```

Output

`[ 10, 20, 30 ]`

## Basic operations on JavaScript arrays

### Accessing elements of an array

Any element in the array can be accessed using the index number. The index in the arrays starts with 0.

```js
// Creating an array and initializing with Values
let a = ["food", "juice", "dessert"];

// Accessing array elements
console.log(a[0]);
console.log(a[1]);
```

Output

```
food
juice
```

### Accessing the first element of an array

The array indexing starts from 0, so we can access first element of array using the index number.

```js
// Creating an Array and Initializing with Values
let a = ["food", "juice", "dessert"];

// Accessing First Array Elements
let fst = a[0];

console.log("First Item: ", fst);
```

Output

`First Item:  food`

### Accessing the last element of an array

We can access the last array element using [array.length – 1] index number.

```js
// Creating an array and initializing with Values
let a = ["food", "soda", "dessert"];

// Accessing Last Array Elements
let lst = a[a.length - 1];

console.log("First Item: ", lst);
```

Output

`First Item:  dessert`

### Modifying the array elements

Elements in an array can be modified by assigning a new value to their corresponding index.

```js
// Creating an array and initializing with Values
let a = ["food", "soda", "dessert"];
console.log(a);

a[1] = "juice";
console.log(a);
```

Output

```
[ 'food', 'soda', 'dessert' ]
[ 'food', 'juice', 'dessert' ]
```

### Adding elements to the array

Elements can be added to the array using methods like push() and unshift().

The push() method adds the element to the end of the array.

The unshift() method adds the element to the starting of the array.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

// Add element to the end of array
a.push("chicken");

// Add element to the beginning
a.unshift("ugali");

console.log(a);
```

Output

`[ 'ugali', 'food', 'soda', 'dessert', 'chicken' ]`

### Removing elements from an array

To remove the elements from an array we have different methods like pop(), shift(), or splice().

The pop() method removes an element from the last index of the array.

The shift() method removes the element from the first index of the array.

The splice() method removes or replaces the element from the array.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];
console.log("Original array: " + a);

// Removes and returns the last element
let lst = a.pop();
console.log("After removing the last: " + a);

// Removes and returns the first element
let fst = a.shift();
console.log("After removing the first: " + a);

// Removes 2 elements starting from index 1
a.splice(1, 2);
console.log("After removing 2 elements starting from index 1: " + a);
```

Output

```
Original array: food,soda,dessert
After removing the last: food,soda
After removing the first: soda
After removing 2 elements starting from index 1: soda
```

### Array length

We can get the length of the array using the array length property.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

let len = a.length;

console.log("Array length: " + len);
```

Output

`Array Length: 3`

### Increase and decrease the array length

We can increase and decrease the array length using the JavaScript length property.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

// Increase the array length to 7
a.length = 7;

console.log("After increasing length: ", a);

// Decrease the array length to 2
a.length = 2;
console.log("After decreasing length: ", a);
```

Output

```
After increasing length:  [ 'food', 'soda', 'dessert', <4 empty items> ]
After decreasing length:  [ 'food', 'soda' ]
```

### Iterating through array elements

We can iterate array and access array elements using for loop and forEach loop.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

// Iterating through for loop
for (let i = 0; i < a.length; i++) {
  console.log(a[i]);
}
```

Output

```
food
soda
dessert
```

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

// Iterating through forEach loop
a.forEach(function myfunc(x) {
  console.log(x);
});
```

Output

```
food
soda
dessert
```

### Conversion of an array to string

We have a builtin method toString() that converts an array to a string.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

// Convert array ot String
console.log(a.toString());
```

Output

`food,soda,dessert`

### Check the type of an array

The JavaScript typeof operator is used to check the type of an array.

It returns “object” for arrays.

```js
// Creating an array and initializing with values
let a = ["food", "soda", "dessert"];

// Check type of array
console.log(typeof a);
```

Output

`object`

### Recognizing a JavaScript array

There are two methods by which we can recognize a JavaScript array:

- By using Array.isArray() method
- By using instanceof method

```js
const courses = ["food", "soda", "dessert"];
console.log("Using Array.isArray() method: ", Array.isArray(courses));
console.log("Using instanceof method: ", courses instanceof Array);
```

Output

```
Using Array.isArray() method:  true
Using instanceof method:  true
```

Note: A common error is faced while writing the arrays:

`const a = [5]` and `const a = new Array(5)`

The above two statements are not the same.

Output: `This statement creates an array with an element ” [5] “.`
