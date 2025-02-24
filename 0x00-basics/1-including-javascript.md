# JavaScript  
Javascript is a dynamic computer programming language.  
- It is lightweight and an interpreted programming language with object-oriented capabilities.  
- Designed for creating network-centric applications.  
- Complementary to and integrated with Java.  
- Complementary to and integrated with HTML.  
- Open and cross-platform.  
### Advantages of JavaScript  
- Less server interaction.  
- Immediate feedback to the visitors.  
- Increased interactivity.  
- Richer interfaces.   
### Limitations of JavaScript  
- Client-side JavaScript does not allow the reading or writing of files. This has
been kept for security reason.  
- JavaScript cannot be used for networking applications because there is no such
support available.  
- JavaScript doesn't have any multithreading or multiprocessor capabilities.  
### Adding JavaScript to HTML  
#### - Internal Javascript  
JavaScript is written inside a `<script>` tag within the HTML file.  
Placing scripts at the bottom of the `<body>` element improves the display speed, because script interpretation slows down the display. 
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1>JavaScript</h1>
    <script>
      console.log("Hello, world!");
      console.log("This is my first time using JavaScript");
    </script>
  </body>
</html>  
```
#### - External JavaScript  
JavaScript is stored in a separate .js file and linked to the HTML document using the `<script>` tag with a src attribute.  
index.html:  
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>JavaScript</title>
    <script src="app.js"></script>
  </head>
  <body>
    <h1>JavaScript</h1>
  </body>
</html>
```
app.js: 
```js
console.log("Welcome to my page!");
console.log("JavaScript is fun");
```
### Optimizing script loading  
If not loaded correctly, JavaScript can block page rendering.  
The browser parses our HTML code line by line and when it comes across a resource that needs to be downloaded to the page e.g. an image, it sends a request to the server to download this resource. However, when it comes across the script tags to download JavaScript, it stops until the JavaScript has been downloaded, it then executes this JavaScript after it has been downloaded and then continues parsing the HTML. This can end up hurting performance.  
To improve performance, use:  
- **defer** keyword  
This ensures that scripts are loaded after the HTML is fully loaded.  
`<script src="app.js" defer></script>`  
- **async** keyword  
It loads scripts asynchronously and runs them as soon as they are downloaded but may execute JavaScript out of order.  
`<script src="script.js" async></script>`
- **Put the script tag at the very end of the page before the closing body tag.**  
```html
...
    <script src="app.js"></script>
</body>
</html>
```
### Comments  
- **Single line comments** - //This is a comment  
- **Multi-line comments** - /*  
This is  
a comment  
*/                                


