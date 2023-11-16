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
