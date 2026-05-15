Introducing React.
 
Q ) What is React? Why React is known as ‘React’?

React is a JavaScript Library. The name ‘React’ was chosen because the library was designed to allow developers to react to changes in state and data within an application, and to update the user interface in a declarative and efficient manner.

Q ) What is Library?

Library is a collections of prewritten code snippets that can be used and reused to perform certain tasks. A particular JavaScript library code can be plugged into application code which leads to faster development and fewer vulnerabilities to have errors. Examples: React, jQuery

Q ) What is Framework?

Framework provides a basic foundation or structure for a website or an application.
Examples: Angular

Q ) Similarities between Library and Framework?

Frameworks and libraries are code written by third parties to solve regular/common problems or to optimise performance.

Q ) Difference between Library and Framework?

A key difference between the two is Inversion of control. When using a library, the control remains with the developer who tells the application when to call library functions. When using a framework, the control is reversed, which means that the framework tells the developer where code needs to be provided and calls it as it requires.

Q ) What is Emmet?

Emmet is the essential toolkit for web-developers. It allows us
to type shortcuts that are then expanded into full-fledged boiler plate code for writing HTML and CSS.

Q ) Difference between React and ReactDOM ?


In React there are two different libraries with different responsibilities:

React → creates elements and defines UI structure.
ReactDOM → takes those elements and renders them to the browser DOM.

Think of it like this:

React = design the UI

ReactDOM = display the UI in the browser
1. Creating an Element (React)

React’s core job is to create elements.
A React element is just a JavaScript object that describes what the UI should look like.

Example:

const heading = React.createElement(
  "h1",
  null,
  "Hello World"
);

Here React creates an element that describes:

type → "h1"

props → null

content → "Hello World"

the null represents the props object.

Why null?

Because h1 has no attributes.


no className

no id

no style

So React uses:

null

meaning:

“No props are provided.”

So internally React creates something like:

{
  type: "h1",
  props: {
    children: "Hello World"
  }
}

Props are attributes passed to React elements/components to control their behavior, appearance, and data.

if props existed:

React.createElement(
  "h1",
  { id: "title" },
  "Hello"
);

then:

{
  type: "h1",
  props: {
    id: "title",
    children: "Hello"
  }
}


At this point:

Nothing appears on the screen.
It is just a description of UI.

2. Rendering an Element (ReactDOM)

To actually show that element in the browser, ReactDOM is used.

Example:

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(heading);

What happens here:

document.getElementById("root")
Finds a real DOM element in HTML.
ReactDOM.createRoot(...)
Creates a React root container.
root.render(heading)
ReactDOM converts the React element → real DOM node
Then inserts it into the page.

Result in browser:

<h1>Hello World</h1>

