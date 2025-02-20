# Callbacks

A callback function is a function that is passed as an argument to another function and executed later.

Callbacks play an essential role in handling asynchronous tasks like reading files, making API requests, and executing code after certain events. 

A function can accept another function as a parameter.

Callbacks allow one function to call another at a later time.

A callback function can execute after another function has finished.
```js
function greet(name, callback) {
    console.log("Hello, " + name);
    callback();
}

function sayBye() {
    console.log("Goodbye!");
}

greet("Ajay", sayBye);
```
Output
```
Hello, Ajay
Goodbye!
```

JavaScript executes code line by line (synchronously), but sometimes we need to delay execution or wait for a task to complete before running the next function. Callbacks help achieve this by passing a function that is executed later.

### Callbacks for asynchronous execution
```js
console.log("Start");

setTimeout(function () {
    console.log("Inside setTimeout");
}, 2000);

console.log("End");
```
Output
```
Start
End
Inside setTimeout  (after 2 seconds)
```
- setTimeout() is an asynchronous function that takes a callback to execute after 2 seconds.
 
- The rest of the code continues executing without waiting.

### Where are callbacks used?

1. Handling Asynchronous Operations

- API requests (fetching data)

- Reading files (Node.js file system)

- Event listeners (clicks, keyboard inputs)

- Database queries (retrieving data)

2. Callbacks in functions handling operations

When a function needs to execute different behaviors based on input, callbacks make the function flexible.
```js
function calc(a, b, callback) {
    return callback(a, b);
}

function add(x, y) {
    return x + y;
}

function mul(x, y) {
    return x * y;
}

console.log(calc(5, 3, add));    
console.log(calc(5, 3, mul));
```
Output
```
8
15
```
- calculate() receives two numbers and a function (add or multiply).

- The passed function is executed inside calculate().

3. Callbacks in event listeners

JavaScript is event-driven, and callbacks handle user interactions like clicks and key presses.
```js
document.getElementById("myButton").addEventListener("click", function () {
    console.log("Button clicked!");
});
```
Here, the anonymous function is a callback that runs when the button is clicked.

4. Callbacks in API calls (Fetching data)
Callbacks are useful when retrieving data from APIs.
```js
function fetch(callback) {
    fetch("https://jsonplaceholder.typicode.com/todos/1")
        .then(response => response.json())
        .then(data => callback(data))
        .catch(error => console.error("Error:", error));
}

function handle(data) {
    console.log("Fetched Data:", data);
}

fetch(handle);
```
fetchData() gets data from an API and passes it to handleData() for processing.

### Features of JavaScript callbacks

- Asynchronous execution: Handle async tasks like API calls, timers, and events without blocking execution.

- Code reusability: Write modular code by passing different callbacks for different behaviors.

- Event-driven programming: Enable event-based execution (e.g., handling clicks, keypresses).

- Error handling: Pass errors to callbacks for better control in async operations.

- Non-Blocking Execution: Keep the main thread free by running long tasks asynchronously.

### Problems with callbacks

1. Callback hell (Nested callbacks)
When callbacks are nested deeply, the code becomes unreadable and hard to maintain.
```js
function step1(callback) {
    setTimeout(() => {
        console.log("Step 1 completed");
        callback();
    }, 1000);
}

function step2(callback) {
    setTimeout(() => {
        console.log("Step 2 completed");
        callback();
    }, 1000);
}

function step3(callback) {
    setTimeout(() => {
        console.log("Step 3 completed");
        callback();
    }, 1000);
}

step1(() => {
    step2(() => {
        step3(() => {
            console.log("All steps completed");
        });
    });
});
```
As the number of steps increases, the nesting grows deeper, making the code difficult to manage.

2. Error handling issues in callbacks
Error handling can get messy when dealing with nested callbacks.
```js
function divide(a, b, callback) {
    if (b === 0) {
        callback(new Error("Cannot divide by zero"), null);
    } else {
        callback(null, a / b);
    }
}

function result(error, result) {
    if (error) {
        console.log("Error:", error.message);
    } else {
        console.log("Result:", result);
    }
}

divide(10, 2, result);
divide(10, 0, result); 
```
Output
```
Result: 5
Error: Cannot divide by zero
```
Handling errors inside callbacks can complicate code readability.
