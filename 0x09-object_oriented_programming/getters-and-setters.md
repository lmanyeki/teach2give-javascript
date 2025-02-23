# Getters and Setters

Getters and setters allow us to retrieve and modify the values directly without directly changing the object property. 

The getter uses the `get` keyword and the setter uses the `set` keyword to modify and retrieve the values.

### JavaScript Getter (The get Keyword)

This is the method used to get the value of the property. 

Getters are automatically called when the property is accessed.

Getters help us in getting the value of the property.
```js
class P {
    constructor(name) {
        this._name = name;
    }

    get name() {
        return this._name;
    }
}

const res = new P('Anjali');
console.log(res.name);
```
Output

`Anjali`

### Getter vs Regular function

Getters allow properties to be accessed like regular object attributes while still executing logic in the background.

On the other hand, regular functions require explicit method calls and do not provide direct property-like access.

|Feature|Getter (get)|Regular Function|
|---------|-----------|----------|
|Syntax |Accessed like a property (obj.prop)|Called explicitly (obj.method())|
|Readability|Improves readability & simplicity| Requires () which makes it look like a method call|
|Encapsulation|Can restrict direct access to properties|Properties can be easily accessed|

### JavaScript Setter (The set Keyword)

The setter is the method that is used for setting the value of the property with the help of the set keyword.

The setter allows us to set the value of the object in a controlled way.

Setters provide a way to control how data is stored by using internal variables, keeping the object’s state secure.
```js
class P {
    constructor(name) {
        this._name = name;
    }

    set name(newName) {
        this._name = newName;
    }
}

const res = new P('Anjali');
res.name = 'Ayushi'; // Using the setter to change the name
console.log(res._name); // Output: Ayushi
```
Output

`Ayushi`

### Using getters and setters in objects

In objects, we can use the get and set keywords for defining the getter and setter in objects.
```js
const p= {
    n1: "Anurag",
    n2: "Das",
    get Name() {
        return `${this.n1} ${this.n2}`;
    },
    set Name(name) {
        [this.n1, this.n2] = name.split(" ");
    }
};

console.log(p.Name);
p.Name = "Anuj Jain";
console.log(p.Name); 
```
Output
```
Anurag Das
Anuj Jain
```
### Getters and Setters with classes

Getters and setters are commonly used in ES6 classes to control access to private properties.
```js
class R {
    constructor(width, height) {
        this.width = width;
        this.height = height;
    }

    get a() {
        return this.width * this.height;
    }

    set a(value) {
        console.log("Area cannot be set directly.");
    }
}

const rect = new R(10, 5);
console.log(rect.a);
rect.a = 60; 
```
Output
```
50
Area cannot be set directly.
```

### Using getters and setters with private fields

```js
class B {
    #balance; // Private property

    constructor(balance) {
        this.#balance = balance;
    }

    get balance() {
        return this.#balance;
    }

    set balance(amount) {
        if (amount < 0) {
            console.log("Balance cannot be negative!");
        } else {
            this.#balance = amount;
        }
    }
}

const acc = new B(1000);
console.log(acc.balance);
acc.balance = -500;  // "Balance cannot be negative!"
```
Output
```
1000
Balance cannot be negative!
```

### Using Object.defineProperty() for accessors

The Object.defineProperty() method can define getters and setters dynamically.
```js
const u = { name: "Anjali" };

Object.defineProperty(u, "greeting", {
    get: function () {
        return `Hello, ${this.name}!`;
    },
    set: function (newName) {
        this.name = newName;
    }
});

console.log(u.greeting);
u.greeting = "Ayushi";
console.log(u.greeting);
```
Output
```
Hello, Anjali!
Hello, Ayushi!
```
