
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

What is undefined in JavaScript?

Answer: undefined is a primitive value automatically assigned by JavaScript to a variable that has been declared but not initialized.



Temporal Dead Zone (TDZ)

The Temporal Dead Zone is the period between the start of a scope (like a block { } or function) and the line where a let or const variable is declared — during which the variable exists but cannot be accessed.
Answer: Because var is function-scoped, allows re-declaration, and supports hoisting with undefined, it often leads to bugs and confusing behavior.
let and const (introduced in ES6) are block-scoped and safer.

{

  // TDZ starts here
  
  console.log(a); // ❌ ReferenceError
  
  let a = 10;     // TDZ ends here
  
  console.log(a); // ✅ 10
  
}
