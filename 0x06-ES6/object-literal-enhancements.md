# Object literal enhancements

Object literal enhancement is used to group variables from the global scope and form them into javascript objects. 

- It is the process of restructuring or putting back together.
```js
// variable declaration 
var name = "Duke"; 
var color = "Brown"; 
var age = 5; 
  
// Using Object Literal Enhancement 
// Combines all variables into a dog object 
var dog = {name, color, age}; 
console.log(dog); 
```
Output 
```
{
    name:"Duke",
    color:"Brown",
    age:5
}
```
- We can also create object methods with object literal enhancement.
```js
// variable declaration 
var name = "Tike"; 
var color = "Black"; 
var age = 7; 
  
// function declaration 
var bark = function(){ 
    console.log("Woof Woof!!"); 
} 
  
// Using Object Literal Enhancement 
// combines all variables into an anotherDog object 
var anotherDog = {name, color, age, bark}; 
anotherDog.bark();
``` 
Output

`Woof Woof!!`

- We can also use “this” keyword to access the object keys.
```js
    // Variable declaration 
    var name = "Lilly"; 
    var color = "White"; 
    var age = 3; 
  
    // function declaration  
    // using "this" keyword to access the object keys. 
    var barkWithName = function(){ 
        console.log('Woof Woof!!, I am '
        +this.name+' and I am a '
        +this.age+' years old, '
        +this.color+ ' coloured dog.Woof Woof!!'); 
    } 
  
    // Using Object Literal Enhancement 
    // combines all variables into a yetAnotherDog object 
    var yetAnotherDog = {name, color, age, barkWithName}; 
    yetAnotherDog.barkWithName(); 
```
Output 
```
Woof Woof!!, I am lilly and I am a 3 years old,
white coloured dog.Woof Woof!!
```
- When defining object methods, it is no longer necessary to use the function keyword. 

Object literal enhancement allows us to pull global variables into objects and reduces typing by making the function keyword unnecessary.
```js
// Old syntax 
var driver1 = { 
    name: "John", 
    speed: 50, 
    car:"Ferrari", 
    speedUp: function(speedup){ 
         this.speed = this.speed + speedup; 
         console.log("new speed = "+ this.speed) 
    } 
} 
  
// New syntax without function keyword 
const driver2 = { 
    name: "Jane", 
    speed: 60, 
    car:"McLaren", 
    speedUp(speedup){ 
         this.speed = this.speed + speedup; 
         console.log("new speed = "+ this.speed) 
    } 
} 
```