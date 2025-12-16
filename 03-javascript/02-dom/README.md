# DOM Manipulation

## Lesson Overview

The Document Object Model (DOM) is JavaScript's interface to HTML. It allows you to select, modify, create, and delete HTML elements dynamically.

## Key Concepts

### 1. Selecting Elements

```javascript
// By ID
const element = document.getElementById('myId');

// By class (returns collection)
const elements = document.getElementsByClassName('myClass');

// By tag (returns collection)
const paragraphs = document.getElementsByTagName('p');

// Query selector (returns first match)
const element = document.querySelector('.myClass');
const element = document.querySelector('#myId');

// Query all (returns NodeList)
const elements = document.querySelectorAll('.myClass');
```

### 2. Modifying Content

```javascript
// Text content
element.textContent = 'New text';

// HTML content
element.innerHTML = '<strong>Bold text</strong>';

// Attributes
element.setAttribute('src', 'image.jpg');
element.getAttribute('src');
element.removeAttribute('disabled');

// Direct properties
element.id = 'newId';
element.className = 'newClass';
element.href = 'https://example.com';
```

### 3. Styling Elements

```javascript
// Individual styles
element.style.color = 'red';
element.style.backgroundColor = 'blue';
element.style.fontSize = '20px';

// Add/remove classes
element.classList.add('active');
element.classList.remove('hidden');
element.classList.toggle('visible');
element.classList.contains('active'); // true/false
```

### 4. Creating and Adding Elements

```javascript
// Create element
const newDiv = document.createElement('div');
newDiv.textContent = 'Hello';
newDiv.classList.add('myClass');

// Append to parent
parent.appendChild(newDiv);

// Insert before
parent.insertBefore(newDiv, referenceElement);

// Modern methods
parent.append(newDiv);          // Add at end
parent.prepend(newDiv);         // Add at beginning
element.before(newDiv);         // Add before element
element.after(newDiv);          // Add after element
```

### 5. Removing Elements

```javascript
element.remove();
parent.removeChild(child);
```

### 6. Traversing the DOM

```javascript
// Parents
element.parentElement;
element.closest('.ancestor-class');

// Children
element.children;
element.firstElementChild;
element.lastElementChild;

// Siblings
element.nextElementSibling;
element.previousElementSibling;
```

## Practice Problems

1. **[Practice 1: Content Manipulator](./practice-1/README.md)** (Easy)
2. **[Practice 2: Dynamic List](./practice-2/README.md)** (Medium)
3. **[Practice 3: Todo App](./practice-3/README.md)** (Hard)

## Next Steps

Move on to [Events and Interactivity](../03-events/README.md)!
