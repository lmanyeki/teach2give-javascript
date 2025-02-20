# Changing document object model elements

### inner.HTML property

Using the `getElementById()` method: This method gets/identifies the DOM elements using its ID and returns the element.

Example

Use the getElementById() method to change the HTML DOM element in javascript.
```js
        function getHtml() { 
            var Element = document.getElementById("iD1"); 
            alert(Element.innerHTML); 
            Element.style.color = "orange"; 
            Element.innerHTML = "GeeksforGeeks"; 
        } 
```

Using the `getElementByName()` method: This method gets/identifies the DOM element by using its class name and returns the element.

Use the getElementsByName() method of javascript to change the HTML DOM element in javascript.
```js
        function getHtml() { 
            var Element =  
                document.getElementsByClassName("p1"); 
  
            alert(Element[0].innerHTML); 
            Element[0].style.color = "blue"; 
            Element[0].innerHTML = "GeeksforGeeks"; 
        } 
``` 

Using the `getElementsByTagName()`: This method gets/identifies the DOM element using its tag name and returns it.

Example

Use the getElementsByTagName() method of javascript to change the HTML DOM element in javascript.
```js
        function getHtml() { 
            var Element = document.getElementsByTagName("p"); 
            for (var i = 0; i < Element.length; i++) { 
                alert(Element[i].innerHTML); 
                Element[i].innerHTML = "GeeksforGeeks."; 
            } 
        } 
``` 
### outer.HTML property

`getElementsByTagName()` method. 
```js
        function getHtml() { 
            var Element = document.getElementsByTagName("div"); 
            alert(Element[0].outerHTML); 
            Element[0].style.color = "red"; 
            Element[0].outerHTML = "<h1> JavaScript. </h1>"
        } 
```
### Changing the styling of HTML elements

Use `element.style.property = "value"`.

Input the value in double quotes even if it is a number.
```js
const title = document.getElementById("title");
title.style.border = "3px solid red";
title.style.fontSize = "48px";
title.style.borderRadius = "5px";
```

### Changing styling in JavaScript using CSS classes

- `element.classList.add()`: adds one or more class names to an element without removing the existing classes.

- `element.classList.remove()`: removes one or more classes from an element.

- `element.classList.toggle()`: toggles the specified class, it is present, it is removed, if it is absent, it is added.

- `element.classList.contains()`: returns true if an element contains the specified class(es), false otherwise.

- `element.classList.replace()`: replaces an existing class with a new class.

- `element.style.setProperty()`: sets a CSS property on an element (first parameter) and its value (second parameter).