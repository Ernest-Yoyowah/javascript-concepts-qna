# JavaScript Basics Q&A

## Control Flow

1. **Question:** Write an example of a nested if-else statement in JavaScript.

**Answer:**

```javascript
let age = 15;
let isDriving = false;
let isLicenseNew = false;

if (age >= 18) {
  if (isDriving) {
    console.log(`You need a license`);
  } else if (isLicenseNew) {
    console.log(`You need to update your license`);
  } else {
    console.log(`You can drive`);
  }
} else {
  console.log(`You are not old enough to drive`);
}
```

2. **Question:** Explain the purpose of the switch statement and provide an example.

**Answer:**
The purpose of the switch statement in JavaScript is to provide results based on conditions. It allows for multiple cases and includes a default result that you define. The switch statement is often considered clearer, has faster compile time, and is easier to read and write compared to using multiple if and else if statements. It also helps reduce code repetition.

**Example:**

```javascript
let day = "Monday";
let message;

switch (day) {
  case "Monday":
    message = "It's the start of the week";
    break;
  case "Wednesday":
    message = "Halfway through the week";
    break;
  case "Friday":
    message = "Weekend is almost here";
    break;
  default:
    message = "Enjoy your day!";
}

console.log(message);
```

3. **Question:** How would you write a for loop in JavaScript?

**Answer:**
To write a for loop in JavaScript, you start with the `for` keyword followed by parentheses. Inside the parentheses:

- Initialize a variable for the loop counter, often using `let` due to variable scoping (`let i = 0`).
- Set the loop condition, indicating when the loop should end (`i < 10` or `i < arr.length`).
- Specify the increment or decrement of the loop counter (`i++` or `i--`).
  Use semicolons to separate these components. Then, open a block of code within curly braces `{}` to execute or return something.

**Example:**

```javascript
for (let i = 0; i < 10; i++) {
  // Code to be executed in each iteration
  console.log(i);
}
```

4. **Question:** What is the difference between for...in and for...of loops?

**Answer:**
While `for...in` and `for...of` loops share similarities and perform similar tasks, their main difference lies in what they iterate over and the output they provide.

- **`for...in` Loop:**

  - Iterates over enumerable properties of an object, including string objects.
  - When used with arrays, it outputs the indexes of the array, not the values.

  **Example:**

  ```javascript
  let person = { name: "Ernest", age: 20, sex: "male" };

  for (let prop in person) {
    console.log(prop); // Outputs the properties of the object person
  }

  // When used with arrays
  let numbers = [1, 2, 3, 4, 5];
  for (let index in numbers) {
    console.log(index); // Outputs indexes: 0, 1, 2, 3, 4
    // To get actual values, we need to be specific
    console.log(numbers[index]); // Outputs values: 1, 2, 3, 4, 5
  }
  ```

- **`for...of` Loop:**

  - Primarily used with arrays and iterates over the values of iterable objects.
  - Outputs the actual values, not the indexes.

  **Example:**

```javascript
let numbers = [1, 2, 3, 4, 5];

for (let num of numbers) {
  console.log(num); // Outputs values: 1, 2, 3, 4, 5
}
```

5. **Question:** How do you use the `break` and `continue` statements in loops?

**Answer:**
Both the `break` and `continue` statements are built-in features in programming loops but serve different purposes.

- **`continue` Statement:**

  - Used to skip the rest of the code inside a loop for the current iteration if a certain condition is met.

  **Example:**

  ```javascript
  for (let i = 0; i < 5; i++) {
    if (i === 2) {
      continue; // Skip the rest of the loop for i === 2
    }
    console.log(i);
  }
  // Output: 0, 1, 3, 4
  ```

- **`break` Statement:**

  - Used to exit the entire loop prematurely if a certain condition is met, regardless of the loop's normal exit condition.

    **Example:**

  ```javascript
  for (let i = 0; i < 5; i++) {
    if (i === 3) {
      break; // Exit the loop when i === 3
    }
    console.log(i);
  }
  // Output: 0, 1, 2
  ```

16. **Question:** Write a function that returns the factorial of a given number using a loop.

**Answer:**
To create a function that returns the factorial of a given number:

1. First, create the function:

   ```javascript
   const factorialIterative = (n) => {};
   ```

2. Declare and initialize a variable, setting it to 1:

   ```javascript
   let result = 1;
   ```

3. Create a for loop to iterate through the numbers up to the given number and multiply them:

   ```javascript
   for (let i = 1; i <= n; i++) {
     result *= i;
   }
   ```

4. Return the result:

   ```javascript
   return result;
   ```

   **Example:**

```javascript
const factorialIterative = (n) => {
  let result = 1;

  for (let i = 1; i <= n; i++) {
    result *= i;
  }

  return result;
};

// Example usage:
const n = 5;
const result = factorialIterative(n);
console.log(`Factorial of ${n} is: ${result}`);
```
