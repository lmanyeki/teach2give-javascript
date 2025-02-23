# Polymorphism

Polymorphism allows you to call the same method on different objects, and each object responds in its own way.

- Method overriding: A child class overrides a method of its parent class.

Occurs when a subclass provides its own specific implementation of a method that is already defined in its parent class.

When you call this method, JavaScript will use the subclass’s implementation instead of the parent’s, which is a runtime decision.

```js
class Animal {
    speak() {
        console.log("Animal makes a sound");
    }
}

class Dog extends Animal {
    speak() {
        console.log("Dog barks");
    }
}

class Cat extends Animal {
    speak() {
        console.log("Cat meows");
    }
}

const dog = new Dog();
dog.speak(); 

const cat = new Cat();
cat.speak();  
```

Output
```js
Dog barks
Cat meows
```

- Method overloading (simulated)

A function behaves differently based on the number or type of its arguments.

It can be simulated by checking the number or type of arguments passed to a function, and executing different logic based on them.
```js
class Calculator {
    add(a, b) {
        if (b === undefined) {
            return a + a; 
        }
        return a + b; 
    }
}

const calc = new Calculator();
console.log(calc.add(2)); 
console.log(calc.add(2, 3));
```
Output
```
4
5
```

### Polymorphism with functions and objects
```js
class A {
    area(x, y) {
        console.log(x * y);
    }
}
class B extends A {
    area(a, b) {
        super.area(a, b);
        console.log('Class B')
    }
}

let ob = new B();
let output = ob.area(100, 200);
```
Output
```
20000
Class B
```