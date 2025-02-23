# Classes

Classes provide a structured way to create objects with shared properties and methods. They support inheritance, encapsulation, and modularity, making it easier to write object-oriented code.

Syntax
```js
class ClassName {
    constructor() {
        // Initialize properties here
    }
    // Define methods here
    methodName() {
        // Method code
    }
}
```
- The class keyword is used to declare a class.

- The constructor() method is a special method that is automatically called when an instance of the class is created.

- You can define methods inside the class to provide behaviour for objects created from the class.

### Key features of JavaScript classes

- Encapsulation.

- Initializes properties when an object is created.

- Inheritance.

- Code reusability.

- Provides a clear structure for creating and managing objects.

```js
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
    g() {
        console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
    }
}
let p1 = new Person("Pranjal", 20);
p1.g();
```
Output

`Hello, my name is Pranjal and I am 20 years old.`

### Constructor to initialize objects

The constructor is used to initialize the properties of the object when an instance is created.
```js
class Car {
    constructor(make, model, year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }
    d() {
        console.log(`${this.year} ${this.make} ${this.model}`);
    }
}
let my = new Car("Toyota", "Corolla", 2021);
my.d();
```
Output

`2021 Toyota Corolla`


### Inheritance in classes

Inheritance allows one class to extend another, inheriting its properties and methods while adding or overriding functionality.
```js
class Car {
    constructor(make, model, year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }
    di() {
        console.log(`${this.year} ${this.make} ${this.model}`);
    }
}
class ElectricCar extends Car {
    constructor(make, model, year, batteryLife) {
        super(make, model, year);
        this.batteryLife = batteryLife;
    }
    d() {
        console.log(`Battery life: ${this.batteryLife} hours`);
    }
}
let tesla = new ElectricCar("Tesla", "Model S", 2022, 24);
tesla.di()
tesla.d();
```
Output
```
2022 Tesla Model S
Battery life: 24 hours
```

### Creating multiple objects from a class

Using classes to create multiple objects with the same structure but different data.
```js
class Car {
    constructor(make, model, year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }
    d() {
        console.log(`${this.year} ${this.make} ${this.model}`);
    }
}
let c1 = new Car("Toyota", "Corolla", 2021);
let c2 = new Car("Honda", "Civic", 2020);
c1.d();
c2.d(); 
```
Output
```
2021 Toyota Corolla
2020 Honda Civic
```