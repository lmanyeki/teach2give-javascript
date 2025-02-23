# Abstraction 

Abstraction can be defined as the concept of hiding the inner complex workings of an object and exposing only the essential features to the user.

- Hiding complexity as it shows only the necessary details.

- Code is organized in a reusable form, which improves maintainability and readability.

- Important data cannot be directly accessed, they are hidden.

- The code can be reused across different applications.
```js
class P{
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    getD() {
        return `${this.name} is ${this.age} years old.`;
    }
}
const p1 = new P("Anuj", 30);
console.log(p1.getD()); 
```
Output

`Anuj is 30 years old.`

- The class P encapsulates both data (name, age) and behaviour (getD method).

- The getD() method provides a simple, reusable way to retrieve a formatted description.

- Creating an instance (p1) and calling getD() is straightforward, with the underlying logic hidden.

- You can create multiple instances of P, each maintaining its own data while reusing the same logic.

### Implementing abstraction using functions

Functions allow you to wrap complex logic into a reusable block of code, exposing only the function name and parameters.
```js
function a(radius) {
    return Math.PI * radius * radius;
}
console.log(a(5)); 
```
Output

`78.53981633974483`

### Using objects and methods

Classes and objects provide a more structured way to achieve abstraction by bundling related properties and methods into a single unit.
```js
const car = {
    brand: "Toyota",
    start: function() {
        console.log("Car started");
    }
};

car.start();
```
Output

`Car started`

### Using closures

Closures help in abstraction by restricting access to certain variables, making them private.
```js
function Count() {
    let c1 = 0;
    return {
        inc: function() {
            c1++;
            console.log(c1);
        }
    };
}

const c2 = Count();
c2.inc(); 
c2.inc(); 
```
Output
```
1
2
```
### Using classes and encapsulation

ES6 classes help implement abstraction by using constructor functions and private fields (using closures or symbols).
```js
class B{
    #balance;
    constructor(B1) {
        this.#balance = B1;
    }
    deposit(amount) {
        this.#balance += amount;
        console.log(`Deposited: $${amount}`);
    }
    getB() {
        return this.#balance;
    }
}

const a1 = new B(1000);
a1.deposit(500);
console.log(a1.getB()); 
```
Output
```
Deposited: $500
1500
```