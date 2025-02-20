# Spread operator

The spread operator (…) is used to expand an array or object into individual elements. 

It allows you to easily pass elements from an array as separate arguments in a function call or combine multiple arrays into one. 

The spread operator helps to make code more concise and readable when working with arrays or objects.
```js
const n = [1, 2, 3];
const ne = [...n, 4, 5];  
console.log(ne); 
```
Output

`[ 1, 2, 3, 4, 5 ]`

The …n spread operator expands the n array into individual elements, so […n, 4, 5] becomes [1, 2, 3, 4, 5].

The code then logs the new array ne, which contains the original elements plus 4 and 5 at the end.

### Expanding arrays

The spread operator which is denoted by … allows iterable elements (like arrays or objects) to expand into individual elements.
```js
const a1 = [1, 2, 3];
const a2 = [...a1, 4, 5];
console.log(a2)
```
Output

`[ 1, 2, 3, 4, 5 ]`

The spread operator expands a1 into individual elements. These elements are combined with additional values into a2.
…a1 expands [1, 2, 3] into 1, 2, 3.

These elements are placed into a2 alongside 4 and 5.

The resulting array is [1, 2, 3, 4, 5].

### Use cases of spread operator

### Merging arrays

Arrays a1 and a2 are merged using the spread operator. The result is a single combined array.
```js
const a1 = [1, 2];
const a2 = [3, 4];
const merged = [...a1, ...a2];
console.log(merged)
```
Output

`[ 1, 2, 3, 4 ]`

…a1 and …a2 expand the arrays.

Elements from both arrays are combined in order.

The result is [1, 2, 3, 4].

The final result will be stored in the merged variable.
### Cloning arrays

The spread operator creates a shallow copy of the original array. 

The new array, clone, is independent of the original.
```js
const original = [10, 20, 30];
const clone = [...original];
console.log(clone)
```
Output

`[ 10, 20, 30 ]`

…original expands elements into a new array.

Changes to clone won’t affect original.

Both arrays share the same initial data.
### Combining objects

Objects obj1 and obj2 are combined using the spread operator. 

Properties in obj2 override those in obj1.
```js
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const combined = { ...obj1, ...obj2 };
console.log(combined)
```
Output

`{ a: 1, b: 3, c: 4 }`

…obj1 and ….obj2 expand properties into a new object.

Duplicate keys are overridden by later objects.

The result is { a: 1, b: 3, c: 4 }.

In this case b is present as a key in both the objects but the second b overwrites the value of first one.

### Merging arrays

Arrays array1 and array2 are merged using the spread operator. The result is a single combined array.
```js
const a1 = [1, 2];
const a2 = [3, 4];
const merged = [...a1, ...a2];
console.log(merged)
```
Output

`[ 1, 2, 3, 4 ]`

…a1 and …a2 expand the arrays.

Elements from both arrays are combined in order.

The result is [1, 2, 3, 4].

The final result will be stored in the merged variable.

### Combining objects

Objects obj1 and obj2 are combined using the spread operator. Properties in obj2 override those in obj1.
```js
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const combined = { ...obj1, ...obj2 };
console.log(combined)
```
Output

`{ a: 1, b: 3, c: 4 }`

…obj1 and ….obj2 expand properties into a new object.

Duplicate keys are overridden by later objects.

The result is { a: 1, b: 3, c: 4 }.

In this case b is present as a key in both the objects but the second b overwrites the value of first one.