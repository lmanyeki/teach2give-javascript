# Destructuring

Destructuring allows you to extract values from arrays or objects and assign them to variables in a concise and readable way. 

It simplifies code, making it shorter and easier to understand.

### How destructuring works

### Array destructuring

It lets you extract values from an array and assign them to variables, instead of using the array's index.
```js
const fruits = ['apple', 'banana', 'cherry'];
const [first, second] = fruits;
console.log(first);  
console.log(second); 
```
Output
```
apple
banana
```

### Object destructuring
This allows you to extract properties from an object and assign them to variables with the same names.
```js
const obj = { name: 'Mohan', age: 30 };
const { name, age } = obj;
console.log(name); 
console.log(age); 
```
Output
```
Mohan
30
```

### Nested destructuring

It allows you to extract values from objects or arrays within other objects or arrays. 
```js
const obj = { name: 'Shinaya', address: { city: 'Dehradun', zip: '248002' } };
const { name, address: { city, zip } } = obj;
console.log(name); 
console.log(city); 
console.log(zip);  
```
Output
```
Shinaya
Dehradun
248002
```
### Destructuring with rest syntax

You can use the rest syntax (...) to extract some properties and collect the remaining ones into a single object.
```js
const obj = { name: 'Raj', age: 25, country: 'India', profession: 'Engineer' };
const { name, age, ...more } = obj;
console.log(name);         
console.log(age);          
console.log(more); 
```
Output
```
Raj
25
{ country: 'India', profession: 'Engineer' }
```

### Default values

You can set a backup value for variables while destructuring. If something is missing or undefined, the default will be used instead.
```js
const person = {
  name: "Alice",
  age: 25,
};

const {
  name: firstName,
  age: yearsSinceBirth,
  major = "Computer Science",
} = person;

console.log(firstName); // Alice
console.log(yearsSinceBirth); // 25
console.log(major); // Computer Science
```

### Skipping items

In arrays, you can choose to ignore certain values while destructuring, focusing only on the ones you need.
```js
const numbers = [1, 2, 3];
const [, , third] = numbers;

console.log(third); // 3
```

### Destructuring function parameters

Destructuring can be used in function parameters to directly access values from objects passed to the function. 
```js
function greet({ name, age }) {
    console.log(`Hello, ${name}. You are ${age} years old.`);
}
const person = { name: 'Raj', age: 25 };
greet(person); 
```
Output

`Hello, Raj. You are 25 years old.`
