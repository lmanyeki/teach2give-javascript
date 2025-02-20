# Template literals

These are string literals that allow embedded expressions (variables) into your code. 

They are enclosed by backticks (`) instead of single (‘) or double (“) quotes.

Syntax

`string text ${expression} string text`

Backticks (`): Used to define a template literal.

${}: Used to insert expressions inside the string, such as variables, function calls or arithmetic operations.

Example
```js
let a='GFG';
console.log(`hello ${a}`)
```
Output

`hello GFG`

Embedding a variable: The template literal `hello ${a}` is used to insert the value of the variable a (which is ‘GFG’) directly into the string, producing the output “hello GFG”.

Cleaner string concatenation: Instead of using + for string concatenation, template literals allow a more readable and convenient way to embed variables and expressions inside strings.

### String interpolation with expressions

String interpolation lets you insert not just variables but also expressions, like math operations or function results, directly into a string.
```js
let x = 5;
let y = 10;
console.log(`The sum of ${x} and ${y} is ${x + y}`);
```
Output

`The sum of 5 and 10 is 15`

### Multi-line strings with template literals

Template literals allow you to create multi-line strings easily without needing escape characters like \n.
```js
const s = `This is a multi-line
string that spans across
several lines.`;
console.log(s);
```
Output
```
This is a multi-line
string that spans across
several lines.
```

### Tagged template literals

Tagged template literals allow you to customize how the string is processed, providing more control over string creation.
```js
function greet(strings, name) {
    return `${strings[0]}${name.toUpperCase()}${strings[1]}`;
}

const name = 'gfg';
console.log(greet`Hello, ${name}!`);
```
Output

`Hello, GFG!`

### Escaping backticks and dollar signs

In JavaScript, if you need to include backticks or dollar signs inside template literals, you can escape them using a backslash (\).
```js
const s = `This is a backtick: (\`) and this is a dollar sign: \$`;
console.log(s);
```
Output

`This is a backtick: (\) and this is a dollar sign: $`

## Use cases

### Multi-line strings

Template literals support multi-line strings without special characters. This example displays a simple poem.
```js
const poem = `Roses are red,
Violets are blue,
JavaScript is awesome,
And so are you!`;
console.log(poem);
```
Output
```
Roses are red,
Violets are blue,
JavaScript is awesome,
And so are you!
```

### Dynamic expressions

Embedding arithmetic expressions within template literals. This example calculates the sum dynamically.
```js
const a = 5, b = 10;
const result = `Sum of ${a} and ${b} is ${a + b}.`;
console.log(result); 
```
Output

`Sum of 5 and 10 is 15.`

### Tagged templates
Tags process template literals directly, modifying how strings and placeholders are combined.
```js
function tag(strings, ...values) {
    return strings.reduce((acc, str, i) => acc + str + (values[i] || ''), '');
}
const output = tag`Hello, ${"Saran"}!`;
console.log(output);
```
Output

`Hello, Saran!`

### HTML template

Template literals build HTML strings dynamically. This example creates an h1 element.
```js
const title = "Welcome";
const html = `<h1>${title}</h1>`;
console.log(html); 
```
Output

`<h1>Welcome</h1>`

### Conditionals in Templates
Ternary operators evaluate conditions within template literals. This example displays a role based on a condition.
```js
const isAdmin = true;
const userRole = `User role: ${isAdmin ? "Admin" : "Guest"}.`;
console.log(userRole);
```
Output

`User role: Admin.`

### Loops with templates

Loops generate dynamic content within templates. This example creates a list of items.
```js
const items = ["apple", "banana", "cherry"];
const list = `Items: ${items.map(item => `\n- ${item}`)}`;
console.log(list);
```
Output
```
Items: 
- apple,
- banana,
- cherry
```
### Embedding functions

Template literals call functions directly. This example transforms text to uppercase.
```js
const toUpper = str => str.toUpperCase();
const s = `Shouting: ${toUpper("hello")}`;
console.log(s); 
```
Output

`Shouting: HELLO`

### Advantages

- Simplifies string concatenation and formatting.

- Enhances readability with embedded expressions.

- Supports clean multi-line string representation.

- Works seamlessly with modern JavaScript features.

- Reduces errors and improves maintainability.