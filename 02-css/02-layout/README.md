# CSS Layout

## Lesson Overview

CSS layout techniques allow you to control how elements are positioned and arranged on your web pages. Modern CSS provides powerful tools like Flexbox and Grid that make creating responsive, flexible layouts much easier than traditional methods.

## Key Concepts

### 1. Flexbox (Flexible Box Layout)

Flexbox is perfect for one-dimensional layouts (rows or columns).

#### Basic Flexbox
```css
.container {
    display: flex;
    /* Main axis direction */
    flex-direction: row;  /* or column, row-reverse, column-reverse */
    
    /* Align items on main axis */
    justify-content: flex-start;  /* or center, flex-end, space-between, space-around */
    
    /* Align items on cross axis */
    align-items: stretch;  /* or flex-start, center, flex-end, baseline */
    
    /* Wrap items */
    flex-wrap: nowrap;  /* or wrap, wrap-reverse */
    
    /* Gap between items */
    gap: 10px;
}

.item {
    /* Grow to fill space */
    flex-grow: 1;
    
    /* Shrink if needed */
    flex-shrink: 1;
    
    /* Base size */
    flex-basis: 200px;
    
    /* Shorthand */
    flex: 1 1 200px;  /* grow shrink basis */
}
```

#### Common Flexbox Patterns

**Center everything:**
```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
```

**Navigation bar:**
```css
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

**Equal width columns:**
```css
.container {
    display: flex;
}

.column {
    flex: 1;
}
```

### 2. CSS Grid

Grid is perfect for two-dimensional layouts (rows AND columns).

#### Basic Grid
```css
.container {
    display: grid;
    
    /* Define columns */
    grid-template-columns: 200px 1fr 200px;  /* 3 columns */
    /* or */
    grid-template-columns: repeat(3, 1fr);  /* 3 equal columns */
    
    /* Define rows */
    grid-template-rows: 100px auto 50px;
    
    /* Gap between cells */
    gap: 20px;
    /* or separate */
    row-gap: 20px;
    column-gap: 10px;
}

.item {
    /* Span multiple columns */
    grid-column: 1 / 3;  /* From line 1 to line 3 */
    /* or */
    grid-column: span 2;  /* Span 2 columns */
    
    /* Span multiple rows */
    grid-row: 1 / 3;
}
```

#### Grid Template Areas
```css
.container {
    display: grid;
    grid-template-areas:
        "header header header"
        "sidebar main main"
        "footer footer footer";
    grid-template-columns: 200px 1fr 1fr;
    gap: 10px;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

#### Responsive Grid
```css
.container {
    display: grid;
    /* Auto-fit columns, minimum 250px, maximum 1fr */
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}
```

### 3. Positioning

```css
.element {
    position: static;    /* Default, normal flow */
    position: relative;  /* Relative to normal position */
    position: absolute;  /* Relative to positioned parent */
    position: fixed;     /* Relative to viewport */
    position: sticky;    /* Switches between relative and fixed */
}

/* Position offsets */
.element {
    top: 10px;
    right: 10px;
    bottom: 10px;
    left: 10px;
}
```

#### Position Examples

**Absolute positioning:**
```css
.parent {
    position: relative;
}

.child {
    position: absolute;
    top: 0;
    right: 0;
}
```

**Fixed header:**
```css
header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
}
```

**Sticky navigation:**
```css
nav {
    position: sticky;
    top: 0;
    z-index: 100;
}
```

### 4. Responsive Design

#### Media Queries
```css
/* Mobile first approach */
.container {
    padding: 10px;
}

/* Tablet */
@media (min-width: 768px) {
    .container {
        padding: 20px;
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .container {
        padding: 40px;
        max-width: 1200px;
        margin: 0 auto;
    }
}
```

#### Responsive Units
```css
/* Viewport units */
.hero {
    height: 100vh;  /* 100% of viewport height */
    width: 100vw;   /* 100% of viewport width */
}

/* Percentage */
.column {
    width: 50%;
}

/* rem (relative to root font size) */
.text {
    font-size: 1.5rem;
}
```

### 5. Common Layout Patterns

#### Holy Grail Layout
```css
body {
    display: grid;
    grid-template-areas:
        "header header header"
        "nav content aside"
        "footer footer footer";
    grid-template-columns: 200px 1fr 200px;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
}
```

#### Card Grid
```css
.cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
}
```

#### Centered Layout
```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}
```

## Best Practices

1. Use Flexbox for one-dimensional layouts
2. Use Grid for two-dimensional layouts
3. Mobile-first responsive design
4. Use relative units (%, rem, em, vw, vh) over fixed units
5. Test layouts on different screen sizes
6. Use `max-width` instead of `width` for responsive containers
7. Consider accessibility in your layouts

## Practice Problems

Complete these three exercises to master CSS layouts:

1. **[Practice 1: Flexbox Photo Gallery](./practice-1/README.md)** (Easy)
   - Create a responsive photo gallery using Flexbox

2. **[Practice 2: Grid Dashboard](./practice-2/README.md)** (Medium)
   - Build a dashboard layout using CSS Grid

3. **[Practice 3: Responsive Website Layout](./practice-3/README.md)** (Hard)
   - Create a complete responsive website layout with header, sidebar, and content

## Next Steps

Once you've completed all practice problems, move on to [CSS Styling and Design](../03-styling/README.md)!
