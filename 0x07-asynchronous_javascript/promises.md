# Promises

Promises make handling asynchronous operations like API calls, file loadin, or time delays easier. 

- Pending: The task is in the initial state.

- Fulfilled: The task was completed successfully and the result is available.

- Rejected: The task failed and an error is provided.
```js
let checkEven = new Promise((resolve, reject) => {
    let number = 4;
    if (number % 2 === 0) resolve("The number is even!");
    else reject("The number is odd!");
});
checkEven
    .then((message) => console.log(message)) // On success
    .catch((error) => console.error(error)); // On failure
```

Syntax
```js
let promise = new Promise((resolve, reject) => {
    // Perform async operation
    if (operationSuccessful) {
        resolve(“Task successful”);
    } else {
        reject(“Task failed”);
    }
});
```

- resolve(value): Marks the promise as fulfilled and provides a result.

- reject(error): Marks the promise as rejected with an error.

1. Promise.all() method

Waits for all promises to resolve and returns their results as an array. If any promise is rejected, it immediately rejects.
```js
Promise.all([
    Promise.resolve("Task 1 completed"),
    Promise.resolve("Task 2 completed"),
    Promise.reject("Task 3 failed")
])
    .then((results) => console.log(results))
    .catch((error) => console.error(error));
```
Output

`Task 3 failed`

2. Promise.allSettled() method

Waits for all promises to settle (fulfilled or rejected) Method and returns an array of their outcomes.
```js
Promise.allSettled([
    Promise.resolve("Task 1 completed"),
    Promise.reject("Task 2 failed"),
    Promise.resolve("Task 3 completed")
])
    .then((results) => console.log(results));
```
Output
```js
[
  { status: 'fulfilled', value: 'Task 1 completed' },
  { status: 'rejected', reason: 'Task 2 failed' },
  { status: 'fulfilled', value: 'Task 3 completed' }
]
```
3. Promise.race() method

Promise.race() Method resolves or rejects as soon as the first promise settles.
```js
Promise.race([
    new Promise((resolve) =>
        setTimeout(() =>
            resolve("Task 1 finished"), 1000)),
    new Promise((resolve) =>
        setTimeout(() =>
            resolve("Task 2 finished"), 500)),
]).then((result) =>
    console.log(result));
```
Output

`Task 2 finished`

4. Promise.any() method

Promise.any() method resolves with the first fulfilled promise. If all are rejected, it rejects with an AggregateError.
```js
Promise.any([
    Promise.reject("Task 1 failed"),
    Promise.resolve("Task 2 completed"),
    Promise.resolve("Task 3 completed")
])
    .then((result) => console.log(result))
    .catch((error) => console.error(error));
```
Output

`Task 2 completed`

5. Promise.resolve() method

Promise.resolve() method returns a promise that resolves with the given value.
```js
Promise.resolve("Immediate success")
    .then((value) => console.log(value));
```
Output

`Immediate success`

6. Promise.reject() method

Promise.reject() method returns a promise that immediately rejects with a given reason.
```js
Promise.reject("Immediate failure")
    .catch((error) => console.error(error));
```
Output

`Immediate failure`

7. Promise.finally() method

Promise.finally() method runs a cleanup or final code block regardless of the promise’s result (fulfilled or rejected).
```js
Promise.resolve("Task completed")
    .then((result) => console.log(result))
    .catch((error) => console.error(error))
    .finally(() => console.log("Cleanup completed"));
```
Output
```
Task completed
Cleanup completed
```
8. Chaining with Promise.prototype.then() method

Allows sequential execution of promises, passing results to the next .then() method.
```js
Promise.resolve(5)
    .then((value) => value * 2) // Multiplies by 2
    .then((value) => value + 3) // Adds 3
    .then((finalValue) => console.log(finalValue)); // Logs: 13
```
Output

`13`
