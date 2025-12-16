# Practice 2: Arrays and Loops (Medium)

## Objective
Work with arrays, loops, and array methods to manipulate data.

## Requirements
Create functions that:
1. Find the sum of all numbers in an array
2. Find the largest number in an array
3. Filter array to only even numbers
4. Create array of squares from input array
5. Reverse a string

## Solution
<details>
<summary>View Solution</summary>

```javascript
// Sum of array
function sumArray(arr) {
    return arr.reduce((sum, num) => sum + num, 0);
}

// Find maximum
function findMax(arr) {
    return Math.max(...arr);
    // or
    // return arr.reduce((max, num) => num > max ? num : max, arr[0]);
}

// Filter even numbers
function getEvens(arr) {
    return arr.filter(num => num % 2 === 0);
}

// Create squares
function squareNumbers(arr) {
    return arr.map(num => num * num);
}

// Reverse string
function reverseString(str) {
    return str.split('').reverse().join('');
}

// Test
const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
console.log("Sum:", sumArray(numbers));
console.log("Max:", findMax(numbers));
console.log("Evens:", getEvens(numbers));
console.log("Squares:", squareNumbers(numbers));
console.log("Reversed:", reverseString("Hello"));
```

</details>
