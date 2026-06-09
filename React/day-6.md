Consistent Hashing = Consistent hashing in Parcel means generating filenames based on file content. If the content doesn't change, the filename stays the same and the browser uses its cached copy. If the content changes, Parcel creates a new hashed filename, forcing the browser to download the latest version while still benefiting from caching for unchanged files.


Q) What is the difference between the `props` mentioned in a React element and the `props` received inside a React component?

This is a very important concept because the word `props` is used in two related but slightly different contexts in React.

When we create a React element using `React.createElement()`, React creates a JavaScript object that describes the UI. For example, when we write `React.createElement("h1", { id: "title" }, "Hello")`, React creates an element object containing a `type` and a `props` property. Here, `props` are part of the React element itself and act as configuration data describing how that element should be rendered. At this stage, React has only created a blueprint of the UI; nothing has been rendered to the screen yet.

The second use of `props` occurs when React executes a component. Suppose we write a component and use it as `<User name="Bhargav" />`. React first creates an element object whose type is the `User` component and whose `props` contain `{ name: "Bhargav" }`. Later, when React renders the component, it reads the `props` from the element object and passes them as an argument to the component function. In other words, React internally does something similar to `User({ name: "Bhargav" })`. The `props` parameter inside the component is therefore the same object that was previously stored in the React element.

The key idea is that these are not two different sets of data. They are the same data at different stages of React's rendering process. First, the data is stored inside the React element object as `element.props`. Then React passes that same object to the component function, where it becomes the `props` parameter.

This is also where destructuring on the fly comes into the picture. Without destructuring, we access values using `props.name` or `props.age`. With destructuring, we directly extract the required properties in the function parameter itself. React still passes the same `props` object; JavaScript simply extracts the values for us automatically.

In simple terms, the `props` inside a React element are part of the element's configuration or blueprint, while the `props` inside a component are the same object received as a function argument when React executes that component. React first stores the data in the element object and then passes it to the component during rendering.

