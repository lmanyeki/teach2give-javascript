# Events

Events are actions or occurrences that happen in the browser.

They can be triggered by various user interactions or by the browser itself.

### Event types

JavaScript supports a variety of event types.

- Mouse events: click, dblclick, mousemove, mouseover, mouseout

- Keyboard events: keydown, keypress, keyup

- Form events: submit, change, focus, blur

- Window events: load, resize, scroll

Common examples:
|onclick |Triggered when an element is clicked.|
|---------|----------------|
|onmouseover| Fired when the mouse pointer moves over an element.|
|onmouseout |Occurs when the mouse pointer leaves an element.|
|onkeydown |Fired when a key is pressed down.|
|onkeyup |Fired when a key is released.|
|onchange |Triggered when the value of an input element changes.|
|onload |Occurs when a page has finished loading.|
|onsubmit| Fired when a form is submitted.|
|onfocus| Occurs when an element gets focus.|
|onblur |Fired when an element loses focus.|

### Event handling methods

1. Inline HTML Handlers

`<button onclick="alert('Button clicked!')">Click Me</button>`

<button onclick="alert('Button clicked!')">Click Me</button>


2. DOM Property Handlers

```
let btn = document.getElementById("myButton");
btn.onclick = () => {
      alert("Button clicked!");
};
```

3. addEventListener() (Preferred)

```
btn.addEventListener("click", () => {
    alert("Button clicked using addEventListener!");
});
```

addEventListener() is the most versatile and recommended method as it supports multiple event listeners and removal of listeners.
