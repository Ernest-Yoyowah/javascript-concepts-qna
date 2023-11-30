# JavaScript Basics Q&A

## Functions and Scope

1. **Question:** Describe the purpose of a JavaScript function.

**Answer:**
In JavaScript, a function is a block of code designed to perform a specific task. It can take input parameters and return a value or result. Functions are used to organize code, make it reusable, and improve code readability. Here are some of the purposes of using functions in JavaScript:

1. **Encapsulate Logic:**
   Functions allow you to encapsulate specific logic, making it modular and easier to manage.

2. **Promote Code Reuse:**
   By defining functions, you can reuse the same logic in multiple parts of your code, reducing redundancy.

3. **Improve Readability:**
   Functions enhance code readability by breaking down complex tasks into smaller, more understandable units.

4. **Handle Errors:**
   Functions can be structured to handle errors and exceptions, promoting robust error management.

5. **Create Abstractions:**
   Functions enable you to create abstractions, allowing you to focus on the high-level functionality without worrying about implementation details.

**Example:**

```javascript
const areaOfRectangle = (width, height) => {
  return width * height;
};

let result = areaOfRectangle(2, 6);
console.log(result);
```

2. **Question:** Explain the difference between function declarations and function expressions.

**Answer:**
Function declarations and function expressions are both ways to define functions in JavaScript, but they have key differences.

1. **Function Declarations:**

   - Always have a function name.
   - Hoisted to the top of their scope, allowing them to be called from anywhere within that scope, even before they are defined.
   - Stored in memory before code execution, making them always available.

2. **Function Expressions:**
   - Do not have a name (anonymous) or can have a name (named function expression).
   - Are not hoisted, meaning they can only be called from within the scope in which they are defined.
   - Are not available until code execution reaches the line where they are defined.

**Example:**

```javascript
// Function Declaration
function greetDeclaration(name) {
  return `Hello, ${name}!`;
}

// Function Expression (Anonymous)
const greetExpression = function (name) {
  return `Hello, ${name}!`;
};

// Function Expression (Named)
const greetNamedExpression = function greet(name) {
  return `Hello, ${name}!`;
};
```

3. **Question:** What is a callback function, and how would you use it?

**Answer:**
A callback function is a function passed as an argument to another function. Callback functions are commonly used in asynchronous operations, event handling, and error handling. They are executed or "called back" when a specific condition or function is met during execution.

Callback functions are crucial for tasks such as handling the result of an asynchronous operation, responding to user interactions, or managing errors in a non-blocking manner.

**Example:**

```javascript
// Example of using a callback function in asynchronous operation
const fetchData = (url, callback) => {
  // Simulating an asynchronous operation (e.g., fetching data from a server)
  setTimeout(() => {
    const data = { result: "Some data" };
    callback(data);
  }, 1000);
};

// Callback function passed to fetchData
const handleData = (data) => {
  console.log(`Data received: ${data.result}`);
};

// Using the fetchData function with the callback
fetchData("https://api.example.com/data", handleData);
```

4. **Question:** How does JavaScript handle variable scope in functions?

**Answer:**
JavaScript uses variable scope to determine where a variable is declared and accessible. There are two main types: local scope and global scope.

1. **Global Scope:**

   - Variables declared outside functions have a global scope.
   - They are accessible everywhere in the code.

2. **Local Scope:**

   - Variables declared inside functions have a local scope.
   - They are accessible only within the functions where they are defined.

3. **Variable Declaration:**
   - **var:** Function-scoped; accessible within the function where they are defined.
   - **let and const:** Block-scoped; accessible only within the block where they are defined in the code.

**Example:**

```javascript
// Global Scope
var globalVar = "I am global";

const exampleFunction = () => {
  // Local Scope
  var localVar = "I am local";
  let blockVar = "I am block-scoped";

  console.log(globalVar); // Accessible
  console.log(localVar); // Accessible
  console.log(blockVar); // Accessible
};

exampleFunction();
console.log(globalVar); // Accessible
console.log(localVar); // Error: localVar is not defined (outside the function)
console.log(blockVar); // Error: blockVar is not defined (outside the block)
```

5. **Question:** What is a closure, and provide an example of its use?

**Answer:**
A closure in JavaScript refers to the situation involving two functions: an outer function and an inner function, where the inner function has the ability to access variables from the outer function. This occurs due to the concept of nested functions, and closures are powerful for creating private variables and maintaining state.

**Example:**

```javascript
function human() {
  const name = "Ernest";

  // The outer function does not have access to variables declared in the inner function
  console.log(innerText); // Error: innerText is not defined in the outer function

  // The inner function has access to the variable 'name' from the outer function
  function sayHi() {
    console.log(`Hi, I am ${name}`);

    // Variables declared in the inner function are not accessible in the outer function
    const innerText = "Inner text";
  }

  sayHi();
}

human();
```

6. **Question:** Write a function that returns the sum of two numbers.

**Answer:**
To write a function that returns the sum of two numbers, you can use an arrow function. Here's an example:

```javascript
const twoSum = (num1, num2) => {
  return num1 + num2;
};

let result = twoSum(2, 5);
console.log(result); // Output: 7
```

7. **Question:** How do you pass parameters to a function in JavaScript?

**Answer:**
To pass parameters in JavaScript functions, you need to define parameters in the function's parameter list. Parameters act as placeholders for values that will be passed into the function when it is called.

Example:

```javascript
const passParameter = (paraA, paraB, paraC) => {
  // Do something with the parameters
};

// Calling the function and passing values as arguments
passParameter("Ernest", "male", "Software Engineer");
```
