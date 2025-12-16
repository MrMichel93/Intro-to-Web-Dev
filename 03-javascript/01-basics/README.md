# JavaScript Basics

## Lesson Overview

JavaScript is a versatile programming language that runs in the browser. This lesson covers the fundamental concepts you need to start writing JavaScript code.

## Key Concepts

### 1. Including JavaScript

```html
<!-- Inline (not recommended) -->
<button onclick="alert('Hello!')">Click</button>

<!-- Internal -->
<script>
    console.log('Hello World');
</script>

<!-- External (recommended) -->
<script src="script.js"></script>
```

### 2. Variables

```javascript
// let - can be reassigned
let age = 25;
age = 26;

// const - cannot be reassigned
const name = "John";

// var - older way (avoid)
var oldWay = "avoid this";
```

### 3. Data Types

```javascript
// String
let text = "Hello World";
let text2 = 'Single quotes work too';

// Number
let integer = 42;
let decimal = 3.14;

// Boolean
let isTrue = true;
let isFalse = false;

// Array
let colors = ["red", "green", "blue"];
let numbers = [1, 2, 3, 4, 5];

// Object
let person = {
    name: "John",
    age: 30,
    city: "New York"
};

// Null and Undefined
let empty = null;
let notDefined;
```

### 4. Operators

```javascript
// Arithmetic
let sum = 10 + 5;        // 15
let difference = 10 - 5; // 5
let product = 10 * 5;    // 50
let quotient = 10 / 5;   // 2
let remainder = 10 % 3;  // 1

// Comparison
10 == "10"  // true (loose equality)
10 === "10" // false (strict equality)
10 != 5     // true
10 > 5      // true
10 <= 10    // true

// Logical
true && false  // false (AND)
true || false  // true (OR)
!true          // false (NOT)
```

### 5. Functions

```javascript
// Function declaration
function greet(name) {
    return "Hello, " + name;
}

// Function call
let message = greet("Alice");

// Arrow function (modern)
const add = (a, b) => {
    return a + b;
};

// Arrow function (concise)
const multiply = (a, b) => a * b;
```

### 6. Conditionals

```javascript
// if-else
if (age >= 18) {
    console.log("Adult");
} else if (age >= 13) {
    console.log("Teenager");
} else {
    console.log("Child");
}

// Ternary operator
let status = age >= 18 ? "Adult" : "Minor";

// Switch
switch (day) {
    case "Monday":
        console.log("Start of week");
        break;
    case "Friday":
        console.log("End of week");
        break;
    default:
        console.log("Middle of week");
}
```

### 7. Loops

```javascript
// for loop
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// while loop
let count = 0;
while (count < 5) {
    console.log(count);
    count++;
}

// for...of (arrays)
let fruits = ["apple", "banana", "orange"];
for (let fruit of fruits) {
    console.log(fruit);
}

// forEach
fruits.forEach(fruit => {
    console.log(fruit);
});
```

### 8. Array Methods

```javascript
let numbers = [1, 2, 3, 4, 5];

// map - transform each element
let doubled = numbers.map(n => n * 2);

// filter - keep elements that match
let evens = numbers.filter(n => n % 2 === 0);

// reduce - combine into single value
let sum = numbers.reduce((total, n) => total + n, 0);

// find - get first matching element
let found = numbers.find(n => n > 3);
```

### 9. String Methods

```javascript
let text = "Hello World";

text.length;              // 11
text.toUpperCase();       // "HELLO WORLD"
text.toLowerCase();       // "hello world"
text.includes("World");   // true
text.split(" ");          // ["Hello", "World"]
text.replace("World", "JS"); // "Hello JS"
```

### 10. Console Methods

```javascript
console.log("Normal message");
console.error("Error message");
console.warn("Warning message");
console.table([{name: "John", age: 30}]);
```

## Practice Problems

1. **[Practice 1: Variables and Functions](./practice-1/README.md)** (Easy)
2. **[Practice 2: Arrays and Loops](./practice-2/README.md)** (Medium)
3. **[Practice 3: Calculator App](./practice-3/README.md)** (Hard)

## Next Steps

Move on to [DOM Manipulation](../02-dom/README.md)!
