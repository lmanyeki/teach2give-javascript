# Static methods and properties

Static methods are functions that are defined on a class but are not accessible through instances of the class. 

Syntax
```js
class ClassName {
    static methodName() {
        // method logic
    }
}
```

```js
class MathUtils {
    static add(a, b) {
        return a + b;
    }

    static multiply(a, b) {
        return a * b;
    }
}

// Calling static methods on the class
console.log(MathUtils.add(5, 3));
console.log(MathUtils.multiply(4, 6));
```
Output
```
8
24
```
### Static method Math.max()
The getMax() method is a static method that wraps the built-in Math.max() function, demonstrating how static methods can be used to perform operations directly on the class.
```js
class Calc {
    static getMax(...numbers) {
        return Math.max(...numbers);
    }
}
console.log(Calc.getMax(1, 5, 3, 9));
```
Output

`9`

### Static method Array.isArray()
Static methods like checkArray() allow you to check for specific conditions (e.g., checking if a variable is an array) without needing to instantiate the class.


```js
class Validator {
    static check(input) {
        return Array.isArray(input);
    }
}
console.log(Validator.check([1, 2, 3]));
console.log(Validator.check('hello'));
```
### Static method counter

Static methods can be used to manage class-level state, such as a counter, without creating individual instances.

```js
class Count {
    static c = 0;
    static inc() {
        return ++Count.c;
    }
    
    static reset() {
        Count.c = 0;
    }
}
console.log(Count.inc()); 
console.log(Count.inc()); 
Count.reset();
console.log(Count.inc()); 
```
Output
```
1
2
1
```

### Static method factory pattern

Static methods can serve as factory methods to create instances of a class, simplifying object creation and initialization.
```js
class User {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    static create(name, age) {
        return new User(name, age);
    }
}
const user = User.create('Ajay', 30);
console.log(user);
```

### Static method singleton pattern

Static methods can be used to implement design patterns like the Singleton, where only one instance of the class is allowed.
```js
class DB{
    static instance
    constructor()
    {
        if(DB.instance)
        {
            return DB.instance
        }
        DB.instance=this
    }
  static  getinstance()
    {
        if(!DB.instance)
        {
            DB.instance=new DB()
        }
        return DB.instance
    }
}
const obj1=new DB()
const obj2=new DB()
console.log(obj1===obj2)
```
Output

`true`