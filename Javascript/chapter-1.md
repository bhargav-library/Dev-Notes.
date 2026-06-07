
1. What are the two phases of JavaScript code execution?

Answer:

JavaScript executes code in two phases:

Memory Creation Phase (Creation / Hoisting Phase):
JS engine scans the code.
It allocates memory for variables and functions.
Functions are stored entirely; variables (var) are initialized to undefined, while let and const are hoisted but uninitialized.

Code Execution Phase:
Code runs line by line.
Variables get their assigned values.
Functions are executed.

This mechanism allows JS to know about variables and functions before execution, leading to hoisting behavior.
