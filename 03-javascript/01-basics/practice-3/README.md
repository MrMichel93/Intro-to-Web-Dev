# Practice 3: Calculator App (Hard)

## Objective
Build a calculator application using JavaScript objects, functions, and array methods.

## Requirements

Create a calculator with the following features:

1. **Calculator Object with Methods:**
   - `add(a, b)` - Add two numbers
   - `subtract(a, b)` - Subtract b from a
   - `multiply(a, b)` - Multiply two numbers
   - `divide(a, b)` - Divide a by b (handle division by zero)
   - `power(base, exponent)` - Calculate base raised to exponent
   - `squareRoot(n)` - Calculate square root (handle negative numbers)
   - `history` - Array to store calculation history
   - `addToHistory()` - Add calculation to history
   - `getHistory()` - Return all history
   - `clearHistory()` - Clear all history

2. **Calculation History Format:**
   - Store each calculation as: `"5 + 3 = 8"`
   - Include all operations performed
   - Limit history to last 10 calculations

3. **Error Handling:**
   - Return error message for division by zero
   - Return error message for square root of negative
   - Validate inputs are numbers

4. **Testing:**
   - Perform multiple calculations
   - Display history after each operation
   - Test error cases

## Tips
- Use object literal syntax or class
- Use template literals for history strings
- Use `Array.push()` to add to history
- Use `Array.slice(-10)` to keep last 10 items
- Use `typeof` or `isNaN()` for validation

## Solution

<details>
<summary>Click to see solution</summary>

```javascript
const calculator = {
    history: [],
    
    add(a, b) {
        if (typeof a !== 'number' || typeof b !== 'number') {
            return 'Error: Invalid input';
        }
        const result = a + b;
        this.addToHistory(`${a} + ${b} = ${result}`);
        return result;
    },
    
    subtract(a, b) {
        if (typeof a !== 'number' || typeof b !== 'number') {
            return 'Error: Invalid input';
        }
        const result = a - b;
        this.addToHistory(`${a} - ${b} = ${result}`);
        return result;
    },
    
    multiply(a, b) {
        if (typeof a !== 'number' || typeof b !== 'number') {
            return 'Error: Invalid input';
        }
        const result = a * b;
        this.addToHistory(`${a} × ${b} = ${result}`);
        return result;
    },
    
    divide(a, b) {
        if (typeof a !== 'number' || typeof b !== 'number') {
            return 'Error: Invalid input';
        }
        if (b === 0) {
            return 'Error: Cannot divide by zero';
        }
        const result = a / b;
        this.addToHistory(`${a} ÷ ${b} = ${result}`);
        return result;
    },
    
    power(base, exponent) {
        if (typeof base !== 'number' || typeof exponent !== 'number') {
            return 'Error: Invalid input';
        }
        const result = Math.pow(base, exponent);
        this.addToHistory(`${base}^${exponent} = ${result}`);
        return result;
    },
    
    squareRoot(n) {
        if (typeof n !== 'number') {
            return 'Error: Invalid input';
        }
        if (n < 0) {
            return 'Error: Cannot calculate square root of negative number';
        }
        const result = Math.sqrt(n);
        this.addToHistory(`√${n} = ${result}`);
        return result;
    },
    
    addToHistory(calculation) {
        this.history.push(calculation);
        // Keep only last 10 calculations
        if (this.history.length > 10) {
            this.history = this.history.slice(-10);
        }
    },
    
    getHistory() {
        return this.history;
    },
    
    clearHistory() {
        this.history = [];
        console.log('History cleared');
    }
};

// Test the calculator
console.log('Addition:', calculator.add(5, 3));
console.log('Subtraction:', calculator.subtract(10, 4));
console.log('Multiplication:', calculator.multiply(6, 7));
console.log('Division:', calculator.divide(20, 4));
console.log('Power:', calculator.power(2, 3));
console.log('Square Root:', calculator.squareRoot(16));

console.log('\nError cases:');
console.log('Divide by zero:', calculator.divide(10, 0));
console.log('Negative square root:', calculator.squareRoot(-4));

console.log('\nCalculation History:');
console.log(calculator.getHistory());

console.log('\nMore calculations:');
calculator.add(100, 50);
calculator.multiply(12, 12);
calculator.subtract(500, 250);

console.log('\nUpdated History:');
calculator.getHistory().forEach((calc, index) => {
    console.log(`${index + 1}. ${calc}`);
});
```

</details>

