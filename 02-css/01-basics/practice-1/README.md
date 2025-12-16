# Practice 1: Style a Simple Page (Easy)

## Objective

Apply basic CSS styling to an HTML page including colors, fonts, spacing, and basic layout. This exercise will help you understand how to connect CSS to HTML and use fundamental CSS properties.

## Requirements

Create two files:

**index.html** - An HTML page with:
1. Proper HTML5 structure
2. A link to your external stylesheet (`styles.css`)
3. An `<h1>` heading with a page title
4. An `<h2>` subheading
5. Three paragraphs of text
6. An unordered list with 4 items
7. A link to another page

**styles.css** - A stylesheet that includes:
1. Set the body:
   - Background color: light gray (#f5f5f5)
   - Font family: Arial or sans-serif
   - Margin: 20px
2. Style the `<h1>`:
   - Color: navy blue
   - Text aligned to center
   - Font size: 36px
3. Style the `<h2>`:
   - Color: dark gray
   - Border bottom: 2px solid gray
   - Padding bottom: 10px
4. Style paragraphs:
   - Line height: 1.6
   - Color: #333
   - Margin bottom: 15px
5. Style the list:
   - No bullet points (list-style: none)
   - Padding left: 0
6. Style links:
   - Color: blue
   - No underline
   - On hover: underline and change color to red

## Tips

- Use the `<link>` tag in the HTML `<head>` to connect your CSS
- Test your page in a browser to see the styles applied
- Use browser DevTools to experiment with different values
- Remember to save both files in the same directory

## Example Output

Your page should have:
- A centered navy title
- A subheading with an underline
- Well-spaced paragraphs
- A clean list without bullets
- Links that change appearance on hover

## Solution

Try to complete this on your own first!

<details>
<summary>Click to see solution</summary>

**index.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Styled Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Welcome to CSS Styling</h1>
    
    <h2>Introduction to Cascading Style Sheets</h2>
    
    <p>CSS is a powerful language that controls the presentation of HTML documents. It allows developers to separate content from design, making websites easier to maintain and more flexible.</p>
    
    <p>With CSS, you can control colors, fonts, spacing, layouts, and even create animations. The possibilities are nearly endless, and learning CSS is essential for any web developer.</p>
    
    <p>In this exercise, we're applying basic styling to demonstrate fundamental CSS concepts like selectors, properties, and values.</p>
    
    <h2>Key Benefits of CSS</h2>
    
    <ul>
        <li>Separation of content and design</li>
        <li>Reusable styles across multiple pages</li>
        <li>Responsive design capabilities</li>
        <li>Improved page load times</li>
    </ul>
    
    <p>Want to learn more? <a href="https://developer.mozilla.org/en-US/docs/Web/CSS">Visit MDN CSS Documentation</a></p>
</body>
</html>
```

**styles.css:**
```css
/* Body styles */
body {
    background-color: #f5f5f5;
    font-family: Arial, sans-serif;
    margin: 20px;
}

/* Heading 1 styles */
h1 {
    color: navy;
    text-align: center;
    font-size: 36px;
}

/* Heading 2 styles */
h2 {
    color: #333;
    border-bottom: 2px solid gray;
    padding-bottom: 10px;
}

/* Paragraph styles */
p {
    line-height: 1.6;
    color: #333;
    margin-bottom: 15px;
}

/* List styles */
ul {
    list-style: none;
    padding-left: 0;
}

li {
    margin-bottom: 8px;
    color: #333;
}

/* Link styles */
a {
    color: blue;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
    color: red;
}
```

</details>
