# Inheritance

Inheritance allows one class or object to derive properties and behaviours from another. 

JavaScript does this using prototypes, which connect objects in a chain, allowing them to share features effortlessly. 

### Common types of inheritance

### prototype-based inheritance

The prototype stores shared properties and methods, allowing all instances of a type to access them.
```js
function Animal(name) {
    this.name = name;
}
Animal.prototype.speak = function () {
    console.log(`${this.name} makes a sound.`);
};

// Child constructor function
function Dog(name) {
    Animal.call(this, name); // Inherit properties
}

// Inherit methods from Animal
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;

// Adding a new method to Dog
Dog.prototype.bark = function () {
    console.log(`${this.name} barks: Woof!`);
};

// Creating an instance
const myDog = new Dog("Buddy");

myDog.speak(); 
myDog.bark();  
```
Output
```
Buddy makes a sound.
Buddy barks: Woof!
```

### ES6 Class-based inheritance

The child class inherits properties and methods from the parent class.
```js
class one {
    constructor(name) {
        this.name = name
    }
    speaks() {
        return `my name is ${this.name}`
    }
}
class two extends one {
    constructor(name) {
        super(name)
    }
}
const o = new two('Pranjal')
console.log(o.speaks())
```
Output

`my name is Pranjal`

### Mixins for inheritance

This code demonstrates prototypal inheritance and object merging using Object.assign(), allowing a constructor function (Person) to inherit methods from multiple objects (one and two).
```js
const one = {
    speak() {
        return `${this.name} walks`
    }
}
const two = {
    walks() {
        return `${this.name} walks`
    }
}
function Person(name) {
    this.name = name
}
Object.assign(Person.prototype, one, two)
const person1 = new Person('Pranjal')
console.log(person1.speak())
console.log(person1.walks())
```
Output
```
Pranjal walks
Pranjal walks
```

### Inheritance with Object.create()

Object.create() in JavaScript creates a new object that uses another object as its prototype, allowing it to inherit all its properties and methods.
```js
let obj = {
    name: 'Pranjal',
    age: 21,
    prints() {
        return `my name is ${this.name}`
    }
}
let obj1 = Object.create(obj)
obj1.name = 'Hello'
console.log(obj1.age)
console.log(obj1.prints())
```
Output
```
21
my name is Hello
```
### Inheritance with object.setPrototypeOf()
This code demonstrates prototypal inheritance using Object.setPrototypeOf(), which sets one object (two) as the prototype of another (one). This allows one to access properties from two.
```js
const one = {
    speak() {
        return `${this.name} speaks`
    }
}
const two = {
    name: 'Pranjal'
}
Object.setPrototypeOf(one, two)
console.log(one.speak())
```
Output

`Pranjal speaks`
