# JavaScript Basics Q&A

## Variables and Data Types:

1. **Question:** What is the difference between `var`, `let`, and `const` in JavaScript?

   - **Answer:** I will first consider what I will be using the variable for (i.e., whether it may change in the future or not). If it will never change, I will use `const`. If it will change, I will use either `var` or `let` (I prefer `let` in most cases because it is block-scoped, while `var` is function-scoped and also prevents variable hoisting and unintentional redeclaration of variables). I would type the name of the variable (e.g., `greet`) and use the assignment operator (`=`) to initialize the value. Example: `let greet = "Hello"` or `const greet = "Hello"`.

2. **Question:** How would you declare and initialize a variable in JavaScript?

   - **Answer:** I will first consider what I will be using the variable for (i.e., whether it may change in the future or not). If it will never change, I will use `const`. If it will change, I will use either `var` or `let` (I prefer `let` in most cases because it is block-scoped, while `var` is function-scoped and also prevents variable hoisting and unintentional redeclaration of variables). I would type the name of the variable (e.g., `greet`) and use the assignment operator (`=`) to initialize the value. Example: `let greet = "Hello"` or `const greet = "Hello"`.

3. **Question:** Can you explain the concept of Hoisting in JavaScript variables?

- **Answer:** Hoisting is a concept in JavaScript that involves the movement of variable and function declarations to the top of their containing scope during the compilation phase. This allows program execution to occur before the actual declarations in the code. For variables declared and initialized with `var`, they are assigned a default value of `undefined` during hoisting.

Behind the scenes, the code is rearranged to place variable and function declarations at the top, making them accessible even before their actual positions in the code. However, it's important to note that hoisting behaves differently for variables declared with `let` and `const`. While the declarations are hoisted, these variables are not initialized until their actual declaration statement is encountered during the code execution. Attempting to access them before declaration results in a `ReferenceError`.

**Example:**

```javascript
console.log(x); // ReferenceError: x is not defined
let x = 5;
console.log(x); // Output: 5
```

4. **Question:** What are the primitive data types in JavaScript?

**Answer:**
A primitive data type in JavaScript is a data type that is not an object and has no methods or properties. The primitive data types include:

- **Number:** Represents numeric values.
- **String:** Represents textual data.
- **Boolean:** Represents true or false values.
- **Null:** Represents the intentional absence of any object value.
- **Undefined:** Represents an uninitialized variable.
- **Symbol:** Introduced in ECMAScript 6, represents unique and immutable values.

Primitive data types are immutable, meaning their values cannot be changed once they are assigned.

5. **Question:** Explain the difference between == and === in JavaScript.

**Answer:**
Both `==` and `===` are equality operators used for comparing values in JavaScript. However, there is a key difference:

- **`==` (Equality Operator):**

  - Checks for equality of values but performs type coercion if the operands are of different types.
  - For example, `1 == '1'` will evaluate to `true` because the values are considered equal after type coercion.

- **`===` (Strict Equality Operator):**
  - Checks for equality of values and also ensures that the operands are of the same type.
  - For example, `1 === '1'` will evaluate to `false` because the values are not only different but also have different types.

Using `===` is often recommended to avoid unexpected type coercion and ensure a strict comparison of both value and type.

6. **Question:** How do you convert a string to a number in JavaScript?

**Answer:**
There are various ways to convert a string to a number, but one common method is to use the built-in `Number()` function. This function takes a string as a parameter and converts it into a number.

**Example:**

```javascript
let age = "25";
console.log(age + 2); // Output: "252" (concatenation)
age = Number(age);
console.log(age + 2); // Output: 27 (numeric addition)
```

7. **Question:** Describe the purpose of the typeof operator.

**Answer:**
The `typeof` operator is a built-in method in JavaScript used to check the data type of values. It returns an output indicating the type of the operand.

**Example:**

```javascript
let age = 13;
console.log(typeof age); // Output: number
```

8. **Question:** What is the difference between null and undefined?

**Answer:**
The `undefined` value is automatically assigned to a variable with no values. In other words, it is the default value given or assigned to an uninitialized variable.

On the other hand, `null` is intentionally assigned to a variable that will be receiving a value later in the future.

9. **Question:** How do you check if a variable is defined in JavaScript?

**Answer:**
To check if a variable is defined in JavaScript, you can use the built-in `typeof` operator to output the current state of the variable.

**Example:**

```javascript
let name;
if (typeof name === "undefined") {
  console.log(`Not Defined`);
} else {
  console.log(`Defined`);
}
```
