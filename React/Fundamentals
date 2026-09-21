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

Q) What is the difference between React and ReactDOM?

In React, there are two different libraries with different responsibilities. React is responsible for creating elements and defining the UI structure, while ReactDOM takes those elements and renders them into the browser DOM. We can think of it like this: React designs the UI, and ReactDOM displays the UI in the browser.

The main job of React is to create elements. A React element is simply a JavaScript object that describes what the UI should look like. For example, when we write `const heading = React.createElement("h1", null, "Hello World");`, React creates an element that describes the type as `"h1"`, the props as `null`, and the content as `"Hello World"`. The `null` here represents the props object. It is used because the `h1` element has no attributes such as `className`, `id`, or `style`. So React uses `null` to mean that no props are provided. Internally, React creates an object like `{ type: "h1", props: { children: "Hello World" } }`.

Props are attributes passed to React elements or components to control their behavior, appearance, and data. If props are provided, for example `React.createElement("h1", { id: "title" }, "Hello");`, then internally React creates something like `{ type: "h1", props: { id: "title", children: "Hello" } }`. At this stage, nothing appears on the screen because it is only a description of the UI.

To actually display the element in the browser, ReactDOM is used. For example, when we write `const root = ReactDOM.createRoot(document.getElementById("root"));` and then `root.render(heading);`, `document.getElementById("root")` first finds a real DOM element from the HTML file. Then ReactDOM creates a React root container, and `root.render(heading)` converts the React element into a real DOM node and inserts it into the webpage. As a result, “Hello World” becomes visible in the browser.


Q) What is camelCase in JSX, and what are the different types of attributes in JSX?

Camel case is a naming style where the first word starts with a lowercase letter and every next word starts with an uppercase letter. Examples include `backgroundColor`, `fontSize`, `onClick`, and `className`. This style looks like camel humps, which is why it is called camelCase. JSX uses camelCase because JSX is written inside JavaScript, and JavaScript property names usually follow the camelCase naming convention. That is why React uses `className` instead of `class`, `onClick` instead of `onclick`, and `tabIndex` instead of `tabindex`.

For example, in normal HTML we write `<button onclick="test()">Click</button>`, but in JSX we write `<button onClick={test}>Click</button>`. Similarly, in normal CSS we write `background-color: red;` and `font-size: 20px;`, but in JSX inline styling we write `backgroundColor: "red"` and `fontSize: "20px"` because JavaScript object properties use camelCase. React chose this approach because JSX eventually becomes JavaScript objects like `{ className: "title", onClick: handleClick }`. JavaScript identifiers cannot contain hyphens like `background-color`, so React uses `backgroundColor` instead.

The attributes used in JSX are called props in React, and they define an element’s styling, behavior, content, events, and functionality. There are many different types of attributes in JSX. General attributes include `className`, `id`, `style`, and `title`, which are commonly used for styling and identification. Image attributes include `src`, `alt`, `width`, and `height`. Link attributes include `href` and `target`. Form and input attributes include `type`, `placeholder`, `value`, `checked`, `disabled`, and `required`. Event attributes handle user interactions, such as `onClick`, `onChange`, `onSubmit`, and `onMouseOver`. JSX also supports boolean attributes like `hidden` and `required`, as well as custom data attributes like `data-id`.

In JSX, all these attributes become part of the props object. For example, `<input type="text" placeholder="Name" />` internally becomes something like `React.createElement("input", { type: "text", placeholder: "Name" });`. So, attributes in JSX are basically properties passed to React elements to control how they look and behave.




