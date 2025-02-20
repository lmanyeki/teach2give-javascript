# Accessing document object models

### Get HTML element by Id

The user has to add the id to the particular HTML element before accessing the HTML element with the id. 

Syntax

`document.getElementById(element_ID);`

- Parameter - It takes the ID of the element which the user wants to access.

- Return value - It returns the object with the particular ID. If the element with the particular ID isn’t found, it returns the NULL value.
```html
<body>
    <!-- Heading element with GeeksforGeeks id-->
    <h1 id="Geeksforgeeks">
        GeeksforGeeks
    </h1>
    <p>DOM getElementById() Method</p>
    <script>
        // Accessing the element by getElementById method
        let temp = document.getElementById("Geeksforgeeks");
 
        console.log(temp);
        console.log(temp.innerHTML);
    </script>
</body>
```

### Get HTML element by className

When users try to access an element using the className, it returns the collection of all objects that include a particular class.

Syntax
`document.getElementsByClassName(element_classnames);`

- Parameter - It takes the multiple class names of the element which the user wants to access.

- Return value - It returns the collection of objects that have a particular class name. 
```html
<body>
    <!-- Multiple html element with GeeksforGeeks class name -->
    <h1 class="GeeksforGeeks">GeeksforGeeks sample 1</h1>
    <h1 class="GeeksforGeeks">GeeksforGeeks sample 2</h1>
    <h1 class="GeeksforGeeks">GeeksforGeeks sample 3</h1>
 
    <p>DOM getElementsByclassName() Method</p>
    <script>
 
        // Accessing the element by getElementsByclassName method
        let temp = document.getElementsByClassName("GeeksforGeeks");
        console.log(temp[0]);
        console.log(temp[1]);
        console.log(temp[2]);
    </script>
</body>
```

### Get HTML element by Name

This method returns the collection of HTML elements that includes the particular name. 

Users can get the length of the collection using the built-in length method.

Syntax

`document.getElementsByName(element_name);`

- Parameter - It takes the name of the element which the user wants to access.

- Return value - It returns the collection of elements that have a particular name.
```html
<body>
    <!-- Multiple html element with GeeksforGeeks name -->
    <h1 name="GeeksforGeeks">GeeksforGeeks sample 1</h1>
    <h1 name="GeeksforGeeks">GeeksforGeeks sample 2</h1>
    <h1 name="GeeksforGeeks">GeeksforGeeks sample 3</h1>
 
    <p>DOM getElementsByName() Method</p>
    <script>
 
        // Accessing the element by getElementsByName method
        let temp = document.getElementsByName("GeeksforGeeks");
        console.log(temp[0]);
        console.log(temp[1]);
        console.log(temp[2]);
    </script>
</body>

### Get HTML elements by TagName

Here, we are accessing the elements using the tag name instead of using the name of the element.

Syntax

`document.getElementsByTagName(Tag_name);`

- Parameter - It takes a single parameter which is the tag name.

- Return value - It returns the collection of elements that includes the tag which passed as a parameter.
```html
<body>
    <!-- Multiple html element with h1 tag -->
    <h1>GeeksforGeeks sample 1</h1>
    <h1>GeeksforGeeks sample 2</h1>
    <h1>GeeksforGeeks sample 3</h1>
 
    <p>DOM getElementsByTagName() Method</p>
 
    <script>
        // Accessing the element by 
        // getElementsByTagName method
        let temp = document.getElementsByTagName("h1");
        console.log(temp[0]);
        console.log(temp[1]);
        console.log(temp[2]);
    </script>
</body>
```
### Get HTML elements by CSS Selector

The `querySelector()` method returns the first element that matches the particular CSS selector. 

The `querySelectorAll()` method returns all element that matches the particular CSS selector. 

To use id/class as a parameter users have to add the ‘#‘/’.‘ sign before it. 

Syntax

`document.querySelector(selectors);`

`document.querySelectorAll(selectors);`

- Parameter - it accepts different CSS selectors such as class, tag name, and id.

- Return value - The querySelector() method returns the first object that matches the CSS selectors, while the querySelectorAll() method returns a collection of all objects that match the CSS selectors.
```html
<body>
    <!-- html element with classnames and id -->
    <h1 class="gfg1" id="g1">GeeksforGeeks sample 1</h1>
    <h1 class="gfg1" id="g2">GeeksforGeeks sample 2</h1>
    <p class="gfg1">GeeksforGeeks sample 3</p>
 
    <script>
        // Accessing the element by class name 
        // using querySelector
        let temp = document.querySelector(".gfg1");
        console.log(temp);
 
        // Accessing the element by id using querySelector
        temp = document.querySelector("#g2");
        console.log(temp);
 
        // Accessing the element by class name and
        // id using querySelector
        temp = document.querySelector(".gfg1#g2");
        console.log(temp);
 
        // Accessing the element by tag name that
        // includes the particular class
        temp = document.querySelector("p.gfg1");
        console.log(temp);
    </script>
</body>
```

```html
<body>
    <!-- html element with classnames and id -->
    <h1 class="gfg1" id="g1">GeeksforGeeks sample 1</h1>
    <h1 class="gfg1" id="g2">GeeksforGeeks sample 2</h1>
    <p class="gfg1">GeeksforGeeks sample 3</p>
 
    <p class="gfg1">GeeksforGeeks sample 4</p>
 
 
    <script>
 
        // Accessing the element by class name, id and
        // tag name using querySelectorAll
        let temp = document.querySelectorAll("h1.gfg1#g2");
        console.log(temp[0]);
 
        // Accessing the element by tag name using 
        // querySelectorAll
        temp = document.querySelectorAll("p");
        console.log(temp[0]);
        console.log(temp[1]);
    </script>
</body>
```