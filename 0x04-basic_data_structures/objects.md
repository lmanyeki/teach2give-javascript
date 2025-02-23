# Objects

JavaScript objects are collections of properties, where each property is defined as a key-value pair. 

They are used to model real-world entities and complex data structures.

The “Object” class represents the JavaScript data types. 

Objects are quite different from JavaScript’s primitive data types. 

It is used to store different types of key collections and complex entities. 

It can be created by using the Object() method or by using object initializer/literal syntax.

### Syntax

Objects can be created using either the **object literal syntax {}** or the **Object() constructor**.

- objectName.methodName()
```js
// Object creation
let student = {
    name: "Martin",
    class: "12th",
    section: "A",

    studentDetails: function () {
        return this.name + " " + this.class
            + " " + this.section + " ";
    }
};

// Display object data
console.log("STUDENT " + student.studentDetails());
```
Output

`STUDENT Martin 12th A`

### JavaScript object properties
A JavaScript property is a member of an object that associates a key with a value.

### Instance properties

An instance property is a property that has a new copy for every new instance of the class.

- constructor - Returns a reference to the object constructor function that has created the instance of an object. 
```js
		function Types() { }
		let types = [
			new Array(),
			[],
			new Boolean(),
			false,
			new Date(),
			new Error(),
			new Function(),
			new RegExp(),
			/(?:)/
		]
		let j = 0;
		while (j < types.length) {
			types[j].constructor = Types
			types[j] = [types[j].constructor,
			types[j] instanceof Types,
			types[j].toString()]
			++j;
		}
		console.log(types.join('\n'));
```
Output
```js
function Types() { },false,
function Types() { },false,
function Types() { },false,false
function Boolean() { [native code] },false,false
function Types() { },false,Wed Feb 19 2025 11:46:38 GMT+0000 (...
```
### Object methods

JavaScript methods are actions that can be performed on objects. 

### Static methods

If the method is called using the Object class itself then it is called a static method of Object.

- assign() - Copy the values and properties from one or more source objects to a target object.
```js
// creating an object constructor and assigning values to it
const obj1 = { a: 1 };

// creating a target object and copying values and
// properties to it using object.assign() method
// Here, obj1 is the source object
const new_obj = Object.assign({}, obj1);

// Displaying the target object
console.log(new_obj);
```
Output

`{ a: 1 }`

- create() - JavaScript does not have the traditional classes seen in other languages.

```js
	// creating a function which will be the
	// prototype for the object to be created later
	function fruits() {
		this.name = 'fruit 1';
	}
	
	// creating a function to whose object will
	// inherit properties from the prototype
	// using object.create() method
	function
	apple() {
		fruits.call(this);
	}
	
	// creating an object of the apple function which
	// will have properties of the prototype
	// object i.e. fruits
	apple.prototype = Object.create(fruits.prototype);
	const app = new apple();
	
	// Displaying the created object
	console.log(app.name);
```
Output

`fruit 1`

- defineProperty() - Defines a new property directly on an object and returns the object.
```js
const geek1 = {};
Object.defineProperty(geek1, 'prop1', {
	value: 65,
	writable: false
});
geek1.prop1 = 7;
console.log(geek1.prop1);

const geek2 = {};
Object.defineProperty(geek2, 'prop2', {

	value: 54,
	value: 23,
	value: 12 * 9,
});
geek2.prop2;
console.log(geek2.prop2);
```
Output
```js
65
108
```
- defineProperties() - Defines object a new or modifies existing properties directly on an object and it returns the object.
```js
const geek = {};

Object.defineProperties(geek, {
	prop1: {
		value: "geeksforgeeks",
		writable: true
	},
	prop2: {}
});

console.log(geek.prop1);
console.log(geek.prop2);
```
Output
```js
geeksforgeeks
undefined
```
- entries() - Return an array consisting of enumerable property [key, value] pairs of the object.
```js
	// creating an object constructor
	// and assigning values to it
	const obj = { 0: 'adam', 1: 'billy', 2: 'chris' };
	
	// Displaying the enumerable property [key, value]
	// pairs of the object using object.entries() method
	console.log(Object.entries(obj)[1]);
```
Output

`[ '1', 'billy' ]`

- freeze() - There is a method Object.freeze() which is used to freeze an object.

```js
// creating an object constructor and assigning values to it
const obj1 = { property1: 'initial_data' };

// creating a second object which will freeze
// the properties of the first object
const obj2 = Object.freeze(obj1);

// Updating the properties of the frozen object
obj2.property1 = 'new_data';

// Displaying the properties of the frozen object
console.log(obj2.property1);
```
Output

`initial_data`

- fromEntries() - Transform a list of key-value pairs into an object.
```js
	const map1 = new Map([ ['big', 'small'], [1, 0] ]);
	const geek = Object.fromEntries(map1);
	console.log(geek);
	
	const map2 = new Map(
		[['Geek1', 'Intern'],
		['stipend', 'Works basis']]
	);
	const geek1 = Object.fromEntries(map2);
	console.log(geek1);
```
Output
```js
{ '1': 0, big: 'small' }
{ Geek1: 'Intern', stipend: 'Works basis' }
```
- getOwnPropertyDescriptor() - Returns a property descriptor for the own property of a given object.

```js
const geeks1 = {
	prop1: "GeeksforGeeks"
}
const geeks2 = {
	prop2: "Best Platform"
}
const geeks3 = {
	prop3: "And Computer science portal"
}
const descriptor1 = Object.getOwnPropertyDescriptor(geeks1, 'prop1');
const descriptor2 = Object.getOwnPropertyDescriptor(geeks2, 'prop2');
const descriptor3 = Object.getOwnPropertyDescriptor(geeks3, 'prop3');
console.log(descriptor1.enumerable);
console.log(descriptor2.enumerable);
console.log(descriptor1.value);
console.log(descriptor2.value);
console.log(descriptor3.enumerable);
console.log(descriptor3.value);
```
Output
```js
true
true
GeeksforGeeks
Best Platform
true
And Computer science portal
```

- getOwnPropertyNames() - Returns all properties that are present in a given object.
```js
const gfg = {
	val1: "Geek1",
	val2: "Geek2",
	val3: "Geek3",
	val4: "Geek4"
};
console.log(Object.getOwnPropertyNames(gfg));

let gfg2 = { val1: 'Geek1', val2: 'Geek2', val3: 'Geek3' };
console.log(Object.getOwnPropertyNames(gfg2).sort());

Object.getOwnPropertyNames(gfg2).
	forEach(function (val, idx, array) {
		console.log(val + ': ' + gfg2[val]);

	});
```
Output
```js
[ 'val1', 'val2', 'val3', 'val4' ]
[ 'val1', 'val2', 'val3' ]
val1: Geek1
val2: Geek2
val3: Geek3
```

- getOwnPropertySymbols() - Returns an array of all symbol properties that are present in a given object.
```js
	const object1 = {};
	let vala = Symbol('geek1');
	let valb = Symbol.for('geek2');
	
	object1[vala] = 'localSymbol';
	object1[valb] = 'globalSymbol';
	
	const objectSymbols = Object.getOwnPropertySymbols(object1);
	console.log(objectSymbols.length);
	
	const object2 = {};
	let a = Symbol('a');
	let b = Symbol.for('b');
	const objectSymbols1 = Object.getOwnPropertySymbols(object2);
	console.log(objectSymbols1.length);
```
Output
```js
2
0
```
- getPrototypeOf() - Check the prototype of an object that the user has created.

```js
// Creating a simple function
function myfun() { }

// creating a new object
let obj = new myfun();

// getting the prototype
console.log(Object.getPrototypeOf(obj));
```
Output

`{}`

- hasOwn() - Checks if a given property exists or not.
```js
let details = {
	name: "Raj",
	course: "DSA",
	website: "geeksforgeeks.org",
}

console.log(Object.hasOwn(details, 'name'));
console.log(Object.hasOwn(details, 'course'));
console.log(Object.hasOwn(details, 'phone number'));
```
Output
```js
true
true
false
```

- isFrozen( ) - Determine if an object is frozen or not.
```js
	// creating an object constructor and assigning values to it
	const object = {
	property: 'hi geeksforgeeks'
	};
	
	// checking whether the object is frozen or not
	console.log(Object.isFrozen(object));
```
Output

`false`

### Instance methods

If the method is called on an instance of a date object then it is called an instance method.

- defineGetter() - Called when the specified property is looked up.

```js
	let obj = {};
	obj.__defineGetter__('printTen', function() {
	return 10;
	});
	console.log(obj.printTen);
```
Output

`10`

- hasOwnProperty() - Check whether the object has the specified property as its own property.

```js
		function checkProperty() {
			let exampleObj = {};
			exampleObj.height = 100;
			exampleObj.width = 100;

			// Checking for existing property
			result1 = exampleObj.hasOwnProperty("height");

			// Checking for non-existing property
			result2 = exampleObj.hasOwnProperty("breadth");

			console.log(result1);

			console.log(result2);
		}
        checkProperty();
```
Output
```js
true
false
```

- isPrototypeOf() - Checks if an object exists in another object’s prototype chain.
```js
function obj1() { }
function obj2() { }

obj1.prototype = Object.create(obj2.prototype);
const obj3 = new obj1();
console.log(obj1.prototype.isPrototypeOf(obj3));
console.log(obj2.prototype.isPrototypeOf(obj3));
```
Output
```js
true
true
```

- IsEnumerable() - Returns a Boolean indicating whether the specified property is enumerable and is the object’s own property.
```js
	const obj = {};
	const arr = [];
	obj.property = 42;
	arr[0] = 42;
	
	console.log(obj.propertyIsEnumerable('property'));
	console.log(arr.propertyIsEnumerable(0));
	console.log(arr.propertyIsEnumerable('length'));
```
Output
```js
true
true
false
```