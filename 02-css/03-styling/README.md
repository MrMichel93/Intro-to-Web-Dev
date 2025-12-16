# CSS Styling and Design

## Lesson Overview

CSS styling goes beyond basic properties to create beautiful, modern interfaces. This section covers advanced styling techniques including transitions, animations, transforms, and design principles to make your websites stand out.

## Key Concepts

### 1. Transitions

Smooth changes between property values:

```css
.button {
    background-color: blue;
    transition: background-color 0.3s ease;
}

.button:hover {
    background-color: darkblue;
}

/* Multiple properties */
.box {
    transition: all 0.3s ease-in-out;
    /* or specific properties */
    transition: transform 0.3s ease, opacity 0.3s ease;
}
```

### 2. Transforms

Manipulate element appearance:

```css
/* 2D Transforms */
.element {
    transform: translate(50px, 100px);  /* Move */
    transform: rotate(45deg);            /* Rotate */
    transform: scale(1.5);               /* Scale */
    transform: skew(10deg, 5deg);        /* Skew */
}

/* 3D Transforms */
.element {
    transform: rotateX(45deg);
    transform: rotateY(45deg);
    transform: perspective(500px) rotateY(45deg);
}

/* Combine transforms */
.element {
    transform: translate(50px, 50px) rotate(45deg) scale(1.2);
}
```

### 3. Animations

Create keyframe animations:

```css
@keyframes slideIn {
    from {
        transform: translateX(-100%);
        opacity: 0;
    }
    to {
        transform: translateX(0);
        opacity: 1;
    }
}

.element {
    animation: slideIn 0.5s ease-out;
}

/* Animation properties */
.element {
    animation-name: slideIn;
    animation-duration: 1s;
    animation-timing-function: ease-in-out;
    animation-delay: 0.5s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
    animation-fill-mode: forwards;
}

/* Shorthand */
.element {
    animation: slideIn 1s ease-in-out 0.5s infinite alternate forwards;
}
```

### 4. Shadows and Effects

```css
/* Box shadow */
.card {
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    /* Multiple shadows */
    box-shadow: 
        0 2px 4px rgba(0,0,0,0.1),
        0 8px 16px rgba(0,0,0,0.1);
}

/* Text shadow */
h1 {
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

/* Blur */
.element {
    filter: blur(5px);
    backdrop-filter: blur(10px);
}
```

### 5. Gradients

```css
/* Linear gradient */
.element {
    background: linear-gradient(to right, #667eea, #764ba2);
    background: linear-gradient(45deg, red, blue);
    background: linear-gradient(to bottom, 
        rgba(0,0,0,0) 0%,
        rgba(0,0,0,0.8) 100%
    );
}

/* Radial gradient */
.element {
    background: radial-gradient(circle, #667eea, #764ba2);
}
```

### 6. Custom Properties (CSS Variables)

```css
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --spacing: 20px;
    --border-radius: 8px;
}

.element {
    background-color: var(--primary-color);
    padding: var(--spacing);
    border-radius: var(--border-radius);
}

/* Override in specific contexts */
.dark-theme {
    --primary-color: #2c3e50;
    --secondary-color: #27ae60;
}
```

### 7. Modern Selectors

```css
/* :not() pseudo-class */
li:not(:last-child) {
    border-bottom: 1px solid #ccc;
}

/* :nth-child() */
tr:nth-child(even) {
    background-color: #f5f5f5;
}

tr:nth-child(3n) {
    background-color: lightblue;
}

/* ::before and ::after */
.element::before {
    content: "→ ";
    color: blue;
}

.element::after {
    content: "";
    display: block;
    width: 50px;
    height: 3px;
    background: red;
}
```

### 8. Clip Path and Shapes

```css
.element {
    clip-path: circle(50%);
    clip-path: polygon(50% 0%, 100% 100%, 0% 100%);
    clip-path: inset(10px 20px 30px 40px);
}
```

### 9. Modern Effects

```css
/* Glassmorphism */
.glass {
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 10px;
}

/* Smooth scrolling */
html {
    scroll-behavior: smooth;
}

/* Hide scrollbar */
.element::-webkit-scrollbar {
    display: none;
}
```

## Design Principles

1. **Consistency**: Use consistent spacing, colors, and fonts
2. **Hierarchy**: Guide users with clear visual hierarchy
3. **Contrast**: Ensure readability with sufficient contrast
4. **Whitespace**: Don't be afraid of empty space
5. **Alignment**: Align elements for a polished look
6. **Color Theory**: Use complementary color schemes
7. **Accessibility**: Ensure your designs work for everyone

## Practice Problems

Complete these three exercises to master CSS styling:

1. **[Practice 1: Animated Buttons](./practice-1/README.md)** (Easy)
   - Create various button styles with hover effects and animations

2. **[Practice 2: Loading Animations](./practice-2/README.md)** (Medium)
   - Build creative loading spinners and progress indicators

3. **[Practice 3: Modern Landing Page](./practice-3/README.md)** (Hard)
   - Create a stunning landing page with advanced styling techniques

## Next Steps

Congratulations on completing the CSS section! Next, move on to [Part 3: JavaScript](../../03-javascript/README.md) to add interactivity!
