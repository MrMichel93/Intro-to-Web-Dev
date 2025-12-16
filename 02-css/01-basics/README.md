# CSS Basics

## Lesson Overview

CSS (Cascading Style Sheets) is used to control the presentation of HTML documents. It allows you to change colors, fonts, spacing, layouts, and much more. Understanding CSS basics is essential for creating visually appealing websites.

## Key Concepts

### 1. CSS Syntax

CSS consists of rulesets that target HTML elements:

```css
selector {
    property: value;
    another-property: another-value;
}
```

Example:
```css
h1 {
    color: blue;
    font-size: 24px;
}
```

### 2. Ways to Add CSS

#### Inline CSS (not recommended)
```html
<p style="color: red;">This is red text</p>
```

#### Internal CSS (in `<head>`)
```html
<head>
    <style>
        p {
            color: red;
        }
    </style>
</head>
```

#### External CSS (recommended)
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```

### 3. CSS Selectors

#### Element Selector
```css
p {
    color: blue;
}
```

#### Class Selector
```css
.highlight {
    background-color: yellow;
}
```

```html
<p class="highlight">Highlighted text</p>
```

#### ID Selector
```css
#header {
    background-color: navy;
}
```

```html
<div id="header">Header content</div>
```

#### Descendant Selector
```css
article p {
    line-height: 1.6;
}
```

#### Multiple Selectors
```css
h1, h2, h3 {
    font-family: Arial, sans-serif;
}
```

#### Pseudo-classes
```css
a:hover {
    color: red;
}

li:first-child {
    font-weight: bold;
}

input:focus {
    border-color: blue;
}
```

### 4. Common CSS Properties

#### Colors
```css
.element {
    color: red;                    /* Text color */
    background-color: #f0f0f0;     /* Background */
    border-color: rgb(100, 100, 100);
}
```

#### Text Properties
```css
p {
    font-family: Arial, sans-serif;
    font-size: 16px;
    font-weight: bold;
    font-style: italic;
    text-align: center;
    text-decoration: underline;
    line-height: 1.5;
    letter-spacing: 1px;
}
```

#### Box Model Properties
```css
.box {
    width: 300px;
    height: 200px;
    padding: 20px;           /* Inside spacing */
    margin: 10px;            /* Outside spacing */
    border: 2px solid black;
}

/* Individual sides */
.box {
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 10px;
    padding-left: 15px;
    /* Shorthand: padding: 10px 15px; */
}
```

#### Display Properties
```css
.element {
    display: block;        /* Takes full width */
    display: inline;       /* Takes only needed width */
    display: inline-block; /* Inline but with width/height */
    display: none;         /* Hides element */
}
```

### 5. The Box Model

Every HTML element is a box with:
- **Content**: The actual content
- **Padding**: Space inside the border
- **Border**: The border around padding
- **Margin**: Space outside the border

```css
.box {
    width: 200px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
    /* Total width = 200 + 20(left) + 20(right) + 5(left) + 5(right) = 250px */
}

/* Use box-sizing to include padding and border in width */
.box {
    box-sizing: border-box;
    width: 200px;  /* Now total width is 200px */
}
```

### 6. Colors in CSS

```css
/* Named colors */
color: red;

/* Hexadecimal */
color: #FF0000;
color: #F00;  /* Shorthand */

/* RGB */
color: rgb(255, 0, 0);

/* RGBA (with transparency) */
color: rgba(255, 0, 0, 0.5);

/* HSL */
color: hsl(0, 100%, 50%);
```

### 7. Units

```css
/* Absolute units */
width: 100px;      /* Pixels */
width: 2cm;        /* Centimeters */

/* Relative units */
font-size: 1.5em;  /* Relative to parent */
font-size: 2rem;   /* Relative to root */
width: 50%;        /* Percentage of parent */
width: 50vw;       /* 50% of viewport width */
height: 100vh;     /* 100% of viewport height */
```

## Best Practices

1. Use external stylesheets for better organization
2. Use classes for reusable styles, IDs sparingly
3. Keep selectors simple and specific
4. Use meaningful class names (e.g., `.primary-button` not `.blue-button`)
5. Add comments to organize your CSS
6. Use `box-sizing: border-box;` for easier sizing

## Practice Problems

Complete these three exercises to master CSS basics:

1. **[Practice 1: Style a Simple Page](./practice-1/README.md)** (Easy)
   - Apply basic styles to an HTML page with colors, fonts, and spacing

2. **[Practice 2: Card Component](./practice-2/README.md)** (Medium)
   - Create styled card components using the box model and various properties

3. **[Practice 3: Navigation Menu](./practice-3/README.md)** (Hard)
   - Build a styled, interactive navigation menu with hover effects

## Next Steps

Once you've completed all practice problems, move on to [CSS Layout](../02-layout/README.md)!
