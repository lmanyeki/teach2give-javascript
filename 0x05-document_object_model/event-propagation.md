# Event propagation

JavaScript events propagate in two phases:

- Capturing phase: Event travels from the root to the target element. The event handler is first on its parent component and then on the component where it was actually wanted to fire that event handler. In short, it means that the event is first captured by the outermost element and propagated to the inner elements. It is also called trickle down.

- Bubbling phase: Event travels from the target element back to the root. When an event happens on a component, it first runs the event handler on it, then on its parent component, then all the way up on other ancestors’ components. By default, all event handles through this order from center component event to outermost component event.

```
document.querySelector("div").addEventListener("click", () => {
    console.log("Div clicked");
}, true); // Capturing phase

button.addEventListener("click", (e) => {
    console.log("Button clicked");
    e.stopPropagation(); // Stops propagation
});
```

- Setting true in addEventListener makes it capture events during the capturing phase.

- stopPropagation() halts further propagation.
