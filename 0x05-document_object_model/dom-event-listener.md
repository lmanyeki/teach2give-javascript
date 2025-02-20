# Event listener method

The addEventListener() method is used to attach an event handler to a HTML document.

Syntax

`element.addEventListener(event, listener, useCapture);`

### Parameters

- **event**: event can be any valid JavaScript event. Events are used without “on” prefixes like using “click” instead of “onclick” or “mousedown” instead of “onmousedown”.

- **listener(handler function)**: It can be a JavaScript function that responds to the event occurring.

- **useCapture**: It is an optional parameter used to control event propagation. A boolean value is passed where “true” denotes the capturing phase and “false” denotes the bubbling phase.

### Why Use addEventListener()?

- Multiple Event Handlers: Unlike the traditional way of assigning events directly (e.g., element.onclick = function() {}), addEventListener() allows multiple handlers for the same event.

- Flexibility: You can easily remove event listeners or add them dynamically based on conditions.

- Control Over Event Propagation: With the useCapture parameter, you can manage how events propagate through the DOM tree.