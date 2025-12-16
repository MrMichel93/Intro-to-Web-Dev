# Practice 1: Variables and Functions (Easy)

## Objective
Practice declaring variables, writing functions, and working with basic JavaScript syntax.

## Requirements
Create a `script.js` file that:
1. Declares variables for name, age, and favorite color
2. Creates a function that takes a name and returns a greeting
3. Creates a function that calculates the area of a rectangle
4. Creates a function that checks if a number is even or odd
5. Tests all functions with console.log()

## Solution
<details>
<summary>View Solution</summary>

```javascript
// Variables
const name = "Alice";
let age = 25;
const favoriteColor = "blue";

// Greeting function
function greet(name) {
    return `Hello, ${name}! Welcome to JavaScript.`;
}

// Rectangle area function
function calculateRectangleArea(width, height) {
    return width * height;
}

// Even/Odd checker
function isEven(number) {
    if (number % 2 === 0) {
        return true;
    } else {
        return false;
    }
}

// Or using ternary
const isEvenShort = (num) => num % 2 === 0;

// Test functions
console.log(greet(name));
console.log(greet("Bob"));
console.log("Area:", calculateRectangleArea(5, 10));
console.log("Is 4 even?", isEven(4));
console.log("Is 7 even?", isEven(7));
```

</details>
