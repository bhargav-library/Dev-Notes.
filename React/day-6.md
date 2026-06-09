Consistent Hashing = Consistent hashing in Parcel means generating filenames based on file content. If the content doesn't change, the filename stays the same and the browser uses its cached copy. If the content changes, Parcel creates a new hashed filename, forcing the browser to download the latest version while still benefiting from caching for unchanged files.


Q) What is the difference between the `props` mentioned in a React element and the `props` received inside a React component?

This is a very important concept because the word `props` is used in two related but slightly different contexts in React.

When we create a React element using `React.createElement()`, React creates a JavaScript object that describes the UI. For example, when we write `React.createElement("h1", { id: "title" }, "Hello")`, React creates an element object containing a `type` and a `props` property. Here, `props` are part of the React element itself and act as configuration data describing how that element should be rendered. At this stage, React has only created a blueprint of the UI; nothing has been rendered to the screen yet.

The second use of `props` occurs when React executes a component. Suppose we write a component and use it as `<User name="Bhargav" />`. React first creates an element object whose type is the `User` component and whose `props` contain `{ name: "Bhargav" }`. Later, when React renders the component, it reads the `props` from the element object and passes them as an argument to the component function. In other words, React internally does something similar to `User({ name: "Bhargav" })`. The `props` parameter inside the component is therefore the same object that was previously stored in the React element.

The key idea is that these are not two different sets of data. They are the same data at different stages of React's rendering process. First, the data is stored inside the React element object as `element.props`. Then React passes that same object to the component function, where it becomes the `props` parameter.

This is also where destructuring on the fly comes into the picture. Without destructuring, we access values using `props.name` or `props.age`. With destructuring, we directly extract the required properties in the function parameter itself. React still passes the same `props` object; JavaScript simply extracts the values for us automatically.

In simple terms, the `props` inside a React element are part of the element's configuration or blueprint, while the `props` inside a component are the same object received as a function argument when React executes that component. React first stores the data in the element object and then passes it to the component during rendering.

Q) Why is it considered a bad practice to use the array index as a key in React?

In React, the `key` prop helps React uniquely identify items in a list between renders. React uses these keys during its reconciliation process to determine which items have been added, removed, updated, or moved. The goal is to efficiently update only the necessary parts of the UI.

Using the array index as a key may seem convenient, and it often works when the list is completely static. However, problems arise when items are inserted, deleted, reordered, or filtered. This happens because the index represents an item's position in the array, not the item's actual identity.

For example, suppose we have a list containing Apple, Banana, and Mango with keys `0`, `1`, and `2`. If we insert Orange at the beginning of the array, all the existing items shift to new indexes. Apple's key changes from `0` to `1`, Banana's key changes from `1` to `2`, and so on. React then assumes that the component previously associated with key `0` is the same component that should now display Orange. As a result, React may reuse component instances incorrectly.

This becomes especially problematic when list items contain local state, user input, animations, or other component-specific data. A component may preserve the state of a completely different item because React thinks they are the same component due to sharing the same key value.

Instead of using indexes, it is usually better to use a unique and stable identifier such as a database ID, product ID, or user ID. Stable keys allow React to correctly track each item even when the list changes.

Using the array index as a key is generally acceptable only when the list is static, never reordered, never filtered, and never has items inserted or removed. In all other cases, a unique and stable key should be used.

In simple terms, array indexes are tied to positions, while React keys should represent the identity of an item. When positions change, index-based keys can cause React to associate the wrong component with the wrong data, leading to unexpected bugs and incorrect state preservation.




