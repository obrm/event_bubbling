# Event Bubbling

## Introduction

Event Propagation and Event Bubbling are two ways of handling events in the Document Object Model (DOM) when an event occurs on an element and how it moves through the DOM tree.

From a theoretical angle, Event Propagation is the process of an event moving through the DOM tree from the target element (the element that the event occurred on) to the top-level element. There are two types of Event Propagation: capturing and bubbling.

Capturing is when the event is first captured by the top-level element, and then moves down to the target element. Bubbling is the opposite, where the event occurs on the target element and then bubbles up to the top-level element.

Event Bubbling is a type of event propagation where the event propagates from the innermost element to the outermost element, in other words, the event bubbles from the target element to the top-level element. This is the default behavior of events in most web browsers.

From a practical approach, Event Propagation and Event Bubbling are used in many different contexts, such as handling events on multiple elements, modal dialogs, navigation menus, form validation, dynamic UI updates, and event delegation. Understanding how events propagate in the DOM can help developers write more efficient and maintainable code.

One of the most important things to keep in mind when working with events is that events can have multiple handlers attached to them, and these handlers can be attached to different elements in the DOM tree. This means that when an event occurs, all of the handlers will be invoked in the order they were attached. Event Bubbling allows you to handle events on multiple elements at once by attaching a single event listener to a parent element, rather than having to attach an event listener to each individual child element.

## Practical Use Cases

Event propagation and event bubbling are used in many different contexts, but some of the most common use cases include:

1. Handling events on multiple elements: Event bubbling allows you to handle events on multiple elements at once by attaching a single event listener to a parent element, rather than having to attach an event listener to each individual child element.


2. Modal dialogs: When a user clicks on a button to open a modal dialog, the event will typically bubble up to the parent element, allowing you to close the modal dialog when the user clicks outside of it.


3. Navigation menus: When a user clicks on a menu item, the event will typically bubble up to the parent element, allowing you to handle the event and navigate to the appropriate page.


4. Form validation: When a user submits a form, the event will typically bubble up to the parent element, allowing you to handle the event and validate the form data before submitting it to the server.


5. Dynamic UI updates: When a user interacts with a UI element, the event will typically bubble up to the parent element, allowing you to handle the event and update the UI dynamically.


6. Event Delegation: Event delegation is a technique used to handle events on multiple elements by attaching a single event listener to a parent element and then checking if the target of the event is the element you are interested in.


7. Preventing Default behavior: Sometimes it is needed to prevent the default behavior of an event like form submission, when the user clicks on a link, it takes the user to a new page. This can be achieved by using event.preventDefault() method.