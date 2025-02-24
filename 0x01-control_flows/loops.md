# Loops

Loops are used to reduce repetitive tasks by repeatedly executing a block of code as long as a specified condition is true. This makes code more concise and efficient.

The basic loops are: 

### for loop

The for loop repeats a block of code a specific number of times. 

It contains initialization, condition, and increment/decrement in one line.

Syntax:
```js
for (initialization; condition; increment/decrement) {
    // Code to execute
}
```
- Initialization is used to initialize the variable used in the loop.

- Condition is used to evaluate the condition of the initial variable, if the condition returns true, the loop starts over again, if the condition returns false, the loop ends.

- Update is used to update the initialization variable.

Example

```js
for (let i = 1; i <= 3; i++) {
    console.log("Count:", i);
}
```
Output
```
Count: 1
Count: 2
Count: 3
```

### while loop

It executes as long as the condition is true. 

It can be thought of as a repeating if statement. 

Syntax: 
```js
while (condition) {
    // Code to execute
}
```
Example
```js
let i = 0;
while (i < 3) {
    console.log("Number:", i);
    i++;
}
```
Output
```js
Number: 0
Number: 1
Number: 2
```

### do-while loop

This is similar to while loop except it executes the code block at least once before checking the condition.

Syntax:
```js
do {
  /* code of block that will be
     executed at least once even if
     condition is false */
} while (condition);
```
Example
```js
let i = 0;
do {
    console.log("Iteration:", i);
    i++;
} while (i < 3);
```
Output
```js
Iteration: 0
Iteration: 1
Iteration: 2
```

### for-in Loop
It is used to iterate over the properties of an object. 

It only iterates over keys of an object which have their enumerable property set to “true”.

Syntax:
```js
for (let key in object) {
    // Code to execute
}
```
Example
```js
const obj = { name: "Ashish", age: 25 };
for (let key in obj) {
    console.log(key, ":", obj[key]);
}
```

Output
```js
name : Ashish
age : 25
```

### for-of Loop
This is used to iterate over iterable objects like arrays, strings, or sets. 

It directly iterate the value and has more concise syntax than for loop.

Syntax:
```js
for (let value of iterable) {
    // Code to execute
}
```
Example
```js
let a = [1, 2, 3, 4, 5];
for (let val of a) {
    console.log(val);
}
```

Output
```js
1
2
3
4
5
```
### Choosing the Right Loop
- Use **for loop** when the number of iterations is known.
- Use **while loop** when the condition depends on dynamic factors.
- Use **do-while loop** to ensure the block executes at least once.
- Use **for…in loop** to iterate over object properties.
- Use **for…of loop** for iterating through iterable objects.

### break statement

break statement is used to terminate the execution of the loop or the switch statement when the condition is true.

It is used in the following ways: 

**In Switch Block (To come out of the block)**
```js
const fruit = "Mango";

switch (fruit) {
    case "Apple":
        console.log("Apple is healthy.");
        break;
    case "Mango":
        console.log("Mango is delicious.");
        break;
    default:
        console.log("No fruit chosen.");
}
```
Output

`Mango is delicious.`

**In a For Loop (To come out of the Loop)**

```js
for (let i = 1; i < 6; i++) {
    if (i == 4) break;
    console.log(i);
}
```

Output
```js
1
2
3
```
**while and do-while loop examples**
```js
// Using break in a while loop
let i = 1;
while (i <= 5) {
    console.log(i);
    if (i === 3) {
        break;
    }
    i++;
}
```
Output
```js
1
2
3
```
```js
// Using break in a do-while loop
let j = 1;
do {
    console.log(j);
    if (j === 3) {
        break;
    }
    j++;
} while (j <= 5);
```
Output
```js
1
2
3
```

### continue statement

The continue statement is used to break the iteration of the loop and follow with the next iteration.

Example of continue to print only odd Numbers smaller than 10
```js
for (let i = 0; i < 10; i++) {
    if (i % 2 == 0) continue;
    console.log(i);
}
```

Output
```js
1
3
5
7
9
```
**How does ***continue*** work?**

- If continue is used in a for loop, the control flow jumps to the test expression after skipping the current iteration.

- In a while loop, the current iteration of the loop is skipped and control flow resumes in the next iteration of the loop.

### Continue vs Break
The major difference between the continue and break statement is that the break statement breaks out of the loop completely while continue is used to break one statement and iterate to the next statement. 