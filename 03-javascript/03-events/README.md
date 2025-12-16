# Events and Interactivity

## Lesson Overview

Events allow JavaScript to respond to user actions like clicks, key presses, mouse movements, and more. This is what makes websites interactive.

## Key Concepts

### 1. Event Listeners

```javascript
// Add event listener
element.addEventListener('click', function() {
    console.log('Clicked!');
});

// Arrow function
element.addEventListener('click', () => {
    console.log('Clicked!');
});

// With event object
element.addEventListener('click', (event) => {
    console.log(event.target);
});
```

### 2. Common Events

```javascript
// Mouse events
element.addEventListener('click', handleClick);
element.addEventListener('dblclick', handleDoubleClick);
element.addEventListener('mouseenter', handleMouseEnter);
element.addEventListener('mouseleave', handleMouseLeave);

// Keyboard events
document.addEventListener('keydown', handleKeyDown);
document.addEventListener('keyup', handleKeyUp);

// Form events
form.addEventListener('submit', handleSubmit);
input.addEventListener('input', handleInput);
input.addEventListener('change', handleChange);
input.addEventListener('focus', handleFocus);
input.addEventListener('blur', handleBlur);

// Window events
window.addEventListener('load', handleLoad);
window.addEventListener('resize', handleResize);
window.addEventListener('scroll', handleScroll);
```

### 3. Event Object

```javascript
element.addEventListener('click', (event) => {
    event.preventDefault();     // Prevent default behavior
    event.stopPropagation();    // Stop bubbling
    console.log(event.target);  // Element that triggered
    console.log(event.type);    // Event type
    console.log(event.clientX); // Mouse X position
    console.log(event.clientY); // Mouse Y position
});
```

### 4. Form Handling

```javascript
form.addEventListener('submit', (event) => {
    event.preventDefault();
    
    const formData = new FormData(form);
    const name = formData.get('name');
    const email = formData.get('email');
    
    console.log(name, email);
});
```

## Practice Problems

1. **[Practice 1: Button Click Counter](./practice-1/README.md)** (Easy)
2. **[Practice 2: Form Validator](./practice-2/README.md)** (Medium)
3. **[Practice 3: Interactive Game](./practice-3/README.md)** (Hard)

## Next Steps

Congratulations! You've completed the JavaScript section. Now move on to the [Final Project](../../final-project/README.md)!
