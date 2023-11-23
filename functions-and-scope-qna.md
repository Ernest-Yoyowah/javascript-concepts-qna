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
