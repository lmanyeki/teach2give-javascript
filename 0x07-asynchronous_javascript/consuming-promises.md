# Consuming promises with async/ await

By enabling asynchronous code to appear synchronous, they enhance code readability and make it easier to manage complex asynchronous flows.
```js
async function fetchData() {
  const response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
  const data = await response.json();
  console.log(data);
}

fetchData();
```
Output:
```
{
  userId: 1,
  id: 1,
  title: ....',
  body: ....}
```

Syntax
```js
async function functionName() {
  try {
    const result = await someAsyncFunction();
    console.log(result);
  } catch (error) {
    console.error("Error:", error.message);
  }
}
```
### Async function

The async function allows us to write promise-based code as if it were synchronous. This ensures that the execution thread is not blocked. 

Async functions always return a promise. If a value is returned that is not a promise, JavaScript automatically wraps it in a resolved promise.

Syntax
```js
async function myFunction() {
  return "Hello";
}


const getData = async () => {
    let data = "Hello World";
    return data;
}

getData().then(data => console.log(data));
```
Output

`Hello World`

### Await keyword

The await keyword is used to wait for a promise to resolve. It can only be used within an async block. 

Await makes the code wait until the promise returns a result, allowing for cleaner and more manageable asynchronous code.
```js
const getData = async () => {
    let y = await "Hello World";
    console.log(y);
}

console.log(1);
getData();
console.log(2);
```
Output
```js
1
2
Hello World
```

### Error handling in Async/Await

- resolve: Used when an asynchronous task is completed successfully.

- reject: Used when an asynchronous task fails, providing the reason for failure.
```js
async function fetchData() {
  try {
    let response = await fetch('https://api.example.com/data');
    let data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}
```
### Advantages of Async and Await

- Async and Await allow asynchronous code to be written in a synchronous style, making it easier to read and understand.

- Using try/catch blocks with async/await simplifies error handling.

- Async and Await prevent nested callbacks and complex promise chains, making the code more linear and readable.

- Debugging async/await code is more intuitive since it behaves similarly to synchronous code.