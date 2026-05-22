Q) What is defer?

If we run a web page in the browser using only JavaScript, the problem is that HTML parsing stops. This means the browser stops reading and understanding the HTML code because it is busy downloading and executing the JavaScript code, which can slow down the page loading process.
But if we use defer, the HTML will continue to parse while the JavaScript is being downloaded. After the HTML is fully parsed, the JavaScript will execute.So, defer does not block HTML parsing, executes JavaScript after the HTML loads, and maintains the order of scripts.

Q )What is Async?

If we use `async` in a web page, the browser will continue parsing the HTML while the JavaScript file is being downloaded in the background. This improves page loading speed because HTML parsing does not stop during the download process.

But unlike `defer`, as soon as the JavaScript file finishes downloading, the browser immediately executes it, even if the HTML is still being parsed. During execution, HTML parsing temporarily stops.

So, `async` does not block HTML parsing during download, executes JavaScript as soon as it is ready, and does not guarantee script order.

Q) What is root in React?

Root is a React root object. It represents the place in the HTML where React will control and render the UI.

Creating the React Root

<h1>const root = ReactDOM.createRoot(document.getElementById("root"))</h1>

<h1>root.render(heading)</h1>

A React element is just a JavaScript object that describes what should appear on the screen.


The flow look like this :

JSX

 ↓
 
Babel converts it

 ↓ 

React.createElement()

 ↓
 
React Element (object)

 ↓
 
ReactDOM.render()

 ↓
 
Real DOM

 ↓

Visible UI


Q) Why It Is Called render?


The word render in programming means. To generate and display visual output on the screen.

Q) What is JSX?

JSX is a syntax that lets us write HTML-like code inside JavaScript. But the browser does not directly understand JSX, so it gets converted into React code like this (const element = React.createElement("h1", null, "Hello World");). And Babel is responsible for all this because JSX is actually understood because of Babel. It is Babel that converts JSX into React.createElement().

Q) What is Babel?

Babel is a JavaScript compiler that converts modern JavaScript code into older, browser-compatible JavaScript so that browsers can understand it properly. Babel is needed because browsers do not always understand JSX or newer JavaScript features like ES6+ features.The browser cannot understand JSX directly. Babel converts it into React.createElement("h1", null, "Hello"), which the browser can understand. Similarly, if we write modern JavaScript like const add = (a, b) => a + b;, Babel converts it into older JavaScript syntax like var add = function(a, b) { return a + b; };. Babel basically performs transpilation, which means converting source code from one version into another version. In React, when we write JSX such as "Hello" inside a h1 tag, Babel converts it into React.createElement() behind the scenes. That is why JSX works in React. One important thing to remember is that Babel does not run in the browser. It runs during development or build time using tools like Vite or Webpack.

Q) What is the relationship between Pracel and Babel?

Parcel uses Babel internally. Parcel is a bundler, while Babel is a compiler. The job of Parcel is to manage the project, combine files like JavaScript, CSS, and images, optimize the code, start the development server, and create the production build. On the other hand, the job of Babel is to convert JSX into JavaScript and transform modern JavaScript features into older browser-compatible JavaScript.

Parcel automatically uses Babel whenever it detects JSX or modern JavaScript syntax. The flow works like this: first, you write code using JSX or modern ES6+ JavaScript. Then Parcel reads your files and internally uses Babel to transform the code into browser-compatible JavaScript. After that, Parcel bundles everything together and sends it to the browser.

Q) Does the relationship remain the same if we use Vite or another bundler instead of Parcel with Babel?

Yes, the relationship basically remains the same even if we use Vite or other bundlers instead of Parcel. The bundler and Babel still have different responsibilities. The bundler manages the project, development server, optimization, and production build, while Babel transforms JSX and modern JavaScript into browser-compatible JavaScript. The main difference is how each bundler uses Babel internally. For example, Parcel automatically uses Babel with almost no configuration, while Webpack usually uses Babel through `babel-loader`. Vite mainly uses a faster tool called ESBuild during development, but it can still use Babel when needed through plugins. So the overall flow still remains the same: first you write modern JavaScript or JSX, then the bundler processes the project and uses Babel or another transformer internally, and finally the browser receives browser-compatible JavaScript.

Q) What is camelCase in JSX, and what are the different types of attributes in JSX?

Camel case is a naming style where the first word starts with a lowercase letter and every next word starts with an uppercase letter. Examples include `backgroundColor`, `fontSize`, `onClick`, and `className`. This style looks like camel humps, which is why it is called camelCase. JSX uses camelCase because JSX is written inside JavaScript, and JavaScript property names usually follow the camelCase naming convention. That is why React uses `className` instead of `class`, `onClick` instead of `onclick`, and `tabIndex` instead of `tabindex`.

For example, in normal HTML we write `<button onclick="test()">Click</button>`, but in JSX we write `<button onClick={test}>Click</button>`. Similarly, in normal CSS we write `background-color: red;` and `font-size: 20px;`, but in JSX inline styling we write `backgroundColor: "red"` and `fontSize: "20px"` because JavaScript object properties use camelCase. React chose this approach because JSX eventually becomes JavaScript objects like `{ className: "title", onClick: handleClick }`. JavaScript identifiers cannot contain hyphens like `background-color`, so React uses `backgroundColor` instead.

The attributes used in JSX are called props in React, and they define an element’s styling, behavior, content, events, and functionality. There are many different types of attributes in JSX. General attributes include `className`, `id`, `style`, and `title`, which are commonly used for styling and identification. Image attributes include `src`, `alt`, `width`, and `height`. Link attributes include `href` and `target`. Form and input attributes include `type`, `placeholder`, `value`, `checked`, `disabled`, and `required`. Event attributes handle user interactions, such as `onClick`, `onChange`, `onSubmit`, and `onMouseOver`. JSX also supports boolean attributes like `hidden` and `required`, as well as custom data attributes like `data-id`.

In JSX, all these attributes become part of the props object. For example, `<input type="text" placeholder="Name" />` internally becomes something like `React.createElement("input", { type: "text", placeholder: "Name" });`. So, attributes in JSX are basically properties passed to React elements to control how they look and behave.
















