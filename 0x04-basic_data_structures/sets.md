# Set reference

Set is a collection of items that are unique, meaning no element can be repeated. 

Elements of the set can be iterated in the insertion order. 

A Set can store any type of value, whether primitive or objects.

Syntax:
```
new Set()
Example: This example will show the use of Set() constructor.
```
Example
```
const mySet = new Set();

mySet.add("California");
mySet.add("India");
mySet.add("California");
mySet.add(10);
mySet.add(10);

const myObject = { a: 1, a: 5 };

mySet.add(myObject);

console.log(mySet);
```
Output

`Set(4) { 'California', 'India', 10, { a: 5 } }`

### Instance property

An instance property is a property that has a new copy for every new instance of the class.

**size** - Returns the size of set.
```
// Create a new set using Set() constructor
let myset = new Set();

// Append new elements to the
// set using add() method
myset.add(23);
myset.add(12);

// Print the modified set
console.log(myset);

// As the set has 2 elements,
// it will return 2.
console.log(myset.size);
```
Output
```
Set(2) { 23, 12 }
2
```

**constructor** - Used to create a new instance of set.
```
function func() {
	const set1 = new Set();
	set1.add(7);
	set1.add("mansi");
	set1.add(8);
	console.log(set1.constructor);
}
func();
```
Output

`[Function: Set]`

### Instance method

If the method is called on an instance of a set then it is called an instance method.

- add() - Adds an element to the set with the specified value.
```
// Create a new set using Set() constructor
let myset = new Set();

// Append new elements to the
// set using add() method
myset.add(23);
myset.add(12);

// Print the modified set
console.log(myset);
```
Output

`Set(2) { 23, 12 }`

- clear() - Removes all the elements from the set.
```	
// Create a new set using Set() constructor
let myset = new Set();

// Append new elements to the
// set using add() method
myset.add(23);

// Print the modified set
console.log(myset);
console.log(myset.size);

// The clear() method will remove
// all elements from the set
myset.clear();

// This will return 0 as there
// are no elements present in the Set
console.log(myset.size);
```
Output
```
Set(1) { 23 }
1
0
```
- delete() - Delete specified element if it exists in the set.
```
// Create a new set using Set() constructor
let myset = new Set();

// Append new elements to the set
// using add() method
myset.add(75);
myset.add(12);

// Print the modified set
console.log(myset);

// As 75 exists, it will be removed 
// and it will return true
console.log(myset.delete(75));
console.log(myset);
```
Output
```
Set(2) { 75, 12 }
true
Set(1) { 12 }
```

### Comparison with JavaScript arrays

Sets ensure all values are unique, whereas arrays can have duplicate values.

Sets provide better performance for membership testing and uniqueness checks.

### Creating a set

Creating a Set and adding elements to the set.
```
const set1 = new Set(['apple', 'banana', 'cherry']);
console.log(set1);
```
Output

`Set(3) { 'apple', 'banana', 'cherry' }`

### Adding and deleting elements

Adding new elements and deleting the elements.
```
const set2 = new Set();
set2.add(1);
set2.add(5);
set2.add(5); // Duplicate element will not be added
set2.add('Hello');
console.log(set2); 
set2.delete(5);
console.log(set2);
```
Output
```
Set(3) { 1, 5, 'Hello' }
Set(2) { 1, 'Hello' }
```
### Checking for element existence

Checking for already existing elements.
```
const set3 = new Set(['a', 'b', 'c']);
console.log(set3.has('a'));
console.log(set3.has('z'));
```
Output
```
true
false
```
### Iterating over a set

Iterating over the set and printing one by one.
```
const set4 = new Set([1, 2, 3, 4]);
for (let item of set4) {
  console.log(item);
}
```
Output
```
1
2
3
4
```
### Removing duplicates

Removing the duplicate elements from the array using set.
```
const numbers = [1, 2, 2, 3, 4, 4, 5];
const uniqueNumbers = [...new Set(numbers)];
console.log(uniqueNumbers);
```
Output

`[ 1, 2, 3, 4, 5 ]`