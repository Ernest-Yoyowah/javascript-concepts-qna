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
