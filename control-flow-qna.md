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

12. **Question:** Explain the purpose of the switch statement and provide an example.

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
