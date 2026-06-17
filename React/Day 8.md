Q) What is "Lifting State Up" in React?

In React, lifting state up is a pattern used when multiple components need access to the same piece of data. Instead of storing separate copies of the same state inside each component, we move the state to their closest common parent component and pass it down to the child components using props. This process is called "lifting state up" because the state is moved upward in the component tree.

To understand why this is necessary, consider two components: `TemperatureInput` and `TemperatureDisplay`. Both need access to the same temperature value. If each component maintains its own `temp` state independently, then updating the temperature in one component will not affect the other because their states are completely separate. As a result, the two components can become out of sync.

The correct approach is to store the `temp` state in their common parent component, such as `App`. The parent then passes the temperature value to both child components through props. If one child component needs to update the state, the parent can also pass down the state updater function. When the state changes in the parent, React automatically re-renders all child components that depend on that state, ensuring that they always remain synchronized.

This works because React follows a one-way data flow model. Data flows from parent components to child components through props. Child components do not directly share state with each other. Instead, they communicate by using shared state stored in a common ancestor.

A real-world example can be seen in a food ordering application. Suppose we have a `SearchBar` component where users type search text and a `RestaurantList` component that filters restaurants based on that search text. Since both components depend on the same data, the search text should be stored in their common parent component, typically `App`. The parent passes the search text and update function to the `SearchBar`, while passing only the search text to the `RestaurantList`.

The reason this pattern is called "lifting" state up is because the state originally resides in a child component but is moved upward to a parent component so that multiple children can access it. In general, a good rule of thumb in React is: if multiple components need the same data, store that state in their closest common parent and pass it down as props.

In simple terms, lifting state up means moving shared state to a common parent component so that multiple child components can access and stay synchronized with the same data.
