# Maps

A map is a collection of elements where each element is stored as a key, value pair. 

Map objects can hold both objects and primitive values as either key or value. 

When we iterate over the map object it returns the key, and value pair in the same order as inserted.

### Creating maps

- Passing an Array to new Map()
- Create a Map and use Map.set()
- Passing an Array to new Map()
```
// Create a map by passing an array of key-value pairs to the map constructor
const arrayMap = new Map([
    ['key1', 'value1'],
    ['key2', 'value2'],
    ['key3', 'value3']
]);
 
// Accessing values in the Map
console.log(arrayMap.get('key1'));  // Output: "value1"
console.log(arrayMap.get('key2'));  // Output: "value2"
console.log(arrayMap.get('key3'));  // Output: "value3"
```
Output
```
value1
value2
value3
```
### Create a Map and use Map.set()
```
// Create an empty Map and use Map.set() to add key-value pairs
const setMap = new Map();
 
// Adding key-value pairs using Map.set()
setMap.set('name', 'John');
setMap.set('age', 25);
setMap.set('city', 'New York');
 
// Accessing values in the Map
console.log(setMap.get('name'));  // Output: "John"
console.log(setMap.get('age'));   // Output: 25
console.log(setMap.get('city'));  // Output: "New York"
```
Output
```
John
25
New York
```

- Map()	- Create Map objects in JavaScript.

```
// map1 contains
// 1 => 10
// 2 => 20
// 3 => 30
// 4 => 40
let map1 = new Map([
	[1, 10], [2, 20],
	[3, 30], [4, 40]
]);

console.log("Map1: ");
console.log(map1);
```
Output
```
Map1: 
Map(4) { 1 => 10, 2 => 20, 3 => 30, 4 => 40 }
```

- constructor	- It is used to return the constructor function of Map.	
```
function func() {
	let map1 = new Map([
		[1, 2],
		[2, 3],
		[4, 5]
	]);
	let value = map1.constructor;
	console.log(value);
}
func();
```
Output
`[Function: Map]`

- size - Return the number of keys, and value pairs stored in a map.
```
let GFGmap = new Map();

// Adding key, value pairs to the map
GFGmap.set('1', 'Apple');
GFGmap.set('2', 'Banana');
GFGmap.set('3', 'Mango');

// Printing number of key, value
// pairs stored in the map
console.log(GFGmap.size);
```
Output

`3`

