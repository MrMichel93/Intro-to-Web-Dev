# HTML Forms and Input

## Lesson Overview

HTML forms are essential for collecting user input on websites. They allow users to enter data, make selections, and interact with your web applications. Forms are used everywhere - from login pages to search bars to contact forms.

## Key Concepts

### 1. Basic Form Structure

```html
<form action="/submit" method="POST">
    <!-- Form inputs go here -->
    <button type="submit">Submit</button>
</form>
```

- `action` - Where to send the form data
- `method` - How to send it (GET or POST)

### 2. Text Input Fields

```html
<!-- Single-line text input -->
<label for="username">Username:</label>
<input type="text" id="username" name="username" placeholder="Enter username">

<!-- Password input (hides characters) -->
<label for="password">Password:</label>
<input type="password" id="password" name="password">

<!-- Email input (validates email format) -->
<label for="email">Email:</label>
<input type="email" id="email" name="email">

<!-- Number input -->
<label for="age">Age:</label>
<input type="number" id="age" name="age" min="0" max="120">

<!-- Multi-line text -->
<label for="message">Message:</label>
<textarea id="message" name="message" rows="4" cols="50"></textarea>
```

### 3. Selection Inputs

```html
<!-- Radio buttons (select one) -->
<p>Choose your size:</p>
<input type="radio" id="small" name="size" value="small">
<label for="small">Small</label>

<input type="radio" id="medium" name="size" value="medium">
<label for="medium">Medium</label>

<input type="radio" id="large" name="size" value="large">
<label for="large">Large</label>

<!-- Checkboxes (select multiple) -->
<p>Select toppings:</p>
<input type="checkbox" id="cheese" name="toppings" value="cheese">
<label for="cheese">Cheese</label>

<input type="checkbox" id="pepperoni" name="toppings" value="pepperoni">
<label for="pepperoni">Pepperoni</label>

<!-- Dropdown menu -->
<label for="country">Country:</label>
<select id="country" name="country">
    <option value="">Select a country</option>
    <option value="usa">United States</option>
    <option value="canada">Canada</option>
    <option value="uk">United Kingdom</option>
</select>
```

### 4. Other Input Types

```html
<!-- Date picker -->
<label for="birthday">Birthday:</label>
<input type="date" id="birthday" name="birthday">

<!-- Color picker -->
<label for="color">Favorite Color:</label>
<input type="color" id="color" name="color">

<!-- File upload -->
<label for="file">Upload file:</label>
<input type="file" id="file" name="file">

<!-- Range slider -->
<label for="volume">Volume:</label>
<input type="range" id="volume" name="volume" min="0" max="100">
```

### 5. Form Attributes

```html
<!-- Required field -->
<input type="text" name="username" required>

<!-- Placeholder text -->
<input type="text" placeholder="Enter your name">

<!-- Disabled field -->
<input type="text" disabled>

<!-- Read-only field -->
<input type="text" readonly value="Cannot edit">

<!-- Max length -->
<input type="text" maxlength="10">
```

### 6. Buttons

```html
<!-- Submit button -->
<button type="submit">Submit Form</button>

<!-- Reset button -->
<button type="reset">Clear Form</button>

<!-- Regular button (for JavaScript) -->
<button type="button">Click Me</button>
```

## Best Practices

1. Always use `<label>` tags with inputs for accessibility
2. Use appropriate input types for better mobile experience
3. Add `placeholder` text to guide users
4. Use `required` attribute for mandatory fields
5. Group related inputs using `<fieldset>` and `<legend>`

## Practice Problems

Complete these three exercises to master HTML forms:

1. **[Practice 1: Contact Form](./practice-1/README.md)** (Easy)
   - Create a simple contact form with name, email, and message

2. **[Practice 2: Registration Form](./practice-2/README.md)** (Medium)
   - Build a user registration form with various input types

3. **[Practice 3: Survey Form](./practice-3/README.md)** (Hard)
   - Create a comprehensive survey with multiple input types and validation

## Next Steps

Once you've completed all practice problems, move on to [HTML Semantic Elements](../03-semantic/README.md)!
