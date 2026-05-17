Q) What is defer?

If we run a web page in the browser using only JavaScript, the problem is that HTML parsing stops. This means the browser stops reading and understanding the HTML code because it is busy downloading and executing the JavaScript code, which can slow down the page loading process.
But if we use defer, the HTML will continue to parse while the JavaScript is being downloaded. After the HTML is fully parsed, the JavaScript will execute.So, defer does not block HTML parsing, executes JavaScript after the HTML loads, and maintains the order of scripts.

Q )What is Async?

If we use `async` in a web page, the browser will continue parsing the HTML while the JavaScript file is being downloaded in the background. This improves page loading speed because HTML parsing does not stop during the download process.

But unlike `defer`, as soon as the JavaScript file finishes downloading, the browser immediately executes it, even if the HTML is still being parsed. During execution, HTML parsing temporarily stops.

So, `async` does not block HTML parsing during download, executes JavaScript as soon as it is ready, and does not guarantee script order.

Q) What is root in React?

Root is a React root object. It represents the place in the HTML where React will control and render the UI.

<h1><div id="root"></div></h1>

This div is an empty container where React will insert your UI.

Creating the React Root

const root = ReactDOM.createRoot(document.getElementById("root"));

<h1>root.render(heading)</h1>;

This means:

Take the React element heading and display it inside the root container.



“Take the React element heading and display it inside the root container.
