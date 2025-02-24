# Conditionals

Conditionals allow you to execute different blocks of code based on specific conditions. The statements control behavior in JavaScript and determine whether or not pieces of code can run.

Conditional statements in JavaScript are:

### if statement

The if statement is used for execution of a block of code if a specified condition is true.

The syntax is as follows:

```js
if(condition) 
{
   // Statements to execute if
   // condition is true
}
```
EXAMPLE
```js
if (10 > 5) {
      let outcome = "if block";
}
​
outcome;
```
**OUTPUT**

`"if block"`

The keyword **if** tells JavaScript to start the conditional statement.

**(10 > 5)** is the condition to test, which in this case is true — 10 is greater than 5.

The part contained inside curly braces {} is the block of code to run.

Because the condition passes, the variable outcome is assigned the value "if block".

### if else statement

An if statement can be extended with an else statement, which adds another block to run when the if conditional doesn’t pass.

The syntax is as follows:
```js
if (condition)
{
    // Executes this block if
    // condition is true
}
else
{
    // Executes this block if
    // condition is false
}
```

Example

```js
if ("food" === "soda") {
      let outcome = "if block";
} else {
      let outcome = "else block";
}
outcome;
```
OUTPUT

`"else block"`

In the example above, "food" and "soda" are not equal, so the else block runs and the variable outcome gets the value "else block".

### else if statements

Used when multiple conditions need to be checked sequentially.

The if statements are executed from the top down. As soon as one of the conditions controlling the if is true, the statement associated with that if is executed, and the rest of the ladder is bypassed. If none of the conditions is true, then the final else statement will be executed.

The syntax is as follows:

```js
if (condition)
    statement;
else if (condition)
    statement;
.
.
else
    statement;
```
```js
let i = 20;

if (i == 10)
    console.log("i is 10");
else if (i == 15)
    console.log("i is 15");
else if (i == 20)
    console.log("i is 20");
else
    console.log("i is not present");
```
OUTPUT

`i is 20`

### Switch statement

The switch statement evaluates an expression and executes a block of code based on matching cases. 

It provides an alternative to long if-else chains, improving readability and maintainability, especially when handling multiple conditional branches.

The syntax is as follows:

```js
switch (expression) {
    case value1:
        // code block 1;
        break;
    case value2:
         // code block 2;
        break;
   ...
    default:
       // default code block;
}
```
- Expression is the value that you want to compare.

- Case value1, case value2, etc., represent the possible values of the expression.

- break statement terminates the switch statement. Without it, execution will continue into the next case.

- Default specifies the code to run if none of the cases match the expression.

Example

```js
let day = 3;
let dayName;

switch (day) {
    case 1:
        dayName = "Monday";
        break;
    case 2:
        dayName = "Tuesday";
        break;
    case 3:
        dayName = "Wednesday";
        break;
    case 4:
        dayName = "Thursday";
        break;
    case 5:
        dayName = "Friday";
        break;
    case 6:
        dayName = "Saturday";
        break;
    case 7:
        dayName = "Sunday";
        break;
    default:
        dayName = "Invalid day";
}

console.log(dayName); // Output: Wednesday
```

### Ternary operator

It is a shortcut for writing simple if-else statements. 

It’s also known as the **Conditional Operator** because it works based on a condition. 

It allows you to quickly decide between two values depending on whether a condition is true or false.

It provides a concise way to write if-else statements in a single line.

The syntax is: 

`condition ? expression if condition is true : expression if condition is false`

- Condition: A statement that returns true or false.

- Value if True: What happens if the condition is true?

- Value if False: What happens if the condition is false?

Example

```js
let PMarks = 50;

let res = (PMarks > 39) ? "Pass" : "Fail";

console.log(res);
```
OUTPUT

`Pass`
