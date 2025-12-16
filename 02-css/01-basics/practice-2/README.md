# Practice 2: Card Component (Medium)

## Objective

Create styled card components using the CSS box model, demonstrating understanding of padding, margins, borders, and various styling properties.

## Requirements

Create two files:

**cards.html** - An HTML page with:
1. Proper HTML5 structure
2. A link to `styles.css`
3. A page heading
4. Three article cards, each containing:
   - An image (use placeholder: `https://via.placeholder.com/300x200`)
   - A heading (card title)
   - A paragraph (card description)
   - A "Read More" link

**styles.css** - A stylesheet that styles:

1. **Body:**
   - Background: light color
   - Font family: sans-serif
   - Padding: 20px

2. **Page heading:**
   - Centered
   - Large font size
   - Margin bottom: 40px

3. **Cards container:**
   - Display cards in a row (use inline-block or similar)
   - Centered content

4. **Each card (article):**
   - Width: 300px
   - Background: white
   - Border radius: 8px
   - Box shadow for depth
   - Margin: 10px
   - Display as inline-block
   - Vertical align: top

5. **Card images:**
   - Full width of card
   - Border radius on top corners only
   - Display as block

6. **Card content area:**
   - Padding: 20px

7. **Card heading:**
   - Color: dark
   - Margin top: 0
   - Font size: 24px

8. **Card paragraph:**
   - Line height: 1.5
   - Color: gray
   - Margin bottom: 20px

9. **"Read More" link:**
   - Display as button-like element
   - Padding: 10px 20px
   - Background color: blue
   - Color: white
   - No underline
   - Border radius: 4px
   - Display as inline-block
   - Hover effect: darker background

## Tips

- Use `box-sizing: border-box;` for easier width calculations
- Use `display: inline-block;` for cards to sit side by side
- Box shadow syntax: `box-shadow: 0 2px 8px rgba(0,0,0,0.1);`
- Border radius for specific corners: `border-radius: 8px 8px 0 0;`

## Bonus Challenges

- Add a hover effect that lifts the card (transform: translateY)
- Add a transition for smooth animations
- Create a "featured" card class with different styling
- Add icons or badges to the cards

## Solution

Try to complete this on your own first!

<details>
<summary>Click to see solution</summary>

**cards.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card Components</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Featured Articles</h1>
    
    <div class="cards-container">
        <article class="card">
            <img src="https://via.placeholder.com/300x200" alt="Article thumbnail">
            <div class="card-content">
                <h2>Getting Started with HTML</h2>
                <p>Learn the fundamentals of HTML and create your first web page. Perfect for beginners who want to start their web development journey.</p>
                <a href="#" class="card-link">Read More</a>
            </div>
        </article>
        
        <article class="card">
            <img src="https://via.placeholder.com/300x200" alt="Article thumbnail">
            <div class="card-content">
                <h2>Mastering CSS Layouts</h2>
                <p>Discover modern CSS layout techniques including Flexbox and Grid. Build responsive designs that work on all devices.</p>
                <a href="#" class="card-link">Read More</a>
            </div>
        </article>
        
        <article class="card">
            <img src="https://via.placeholder.com/300x200" alt="Article thumbnail">
            <div class="card-content">
                <h2>JavaScript Essentials</h2>
                <p>Unlock the power of JavaScript to create interactive and dynamic web applications. Learn the core concepts every developer needs.</p>
                <a href="#" class="card-link">Read More</a>
            </div>
        </article>
    </div>
</body>
</html>
```

**styles.css:**
```css
/* Universal box sizing */
* {
    box-sizing: border-box;
}

/* Body styles */
body {
    background-color: #f0f0f0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    padding: 20px;
    margin: 0;
}

/* Page heading */
h1 {
    text-align: center;
    font-size: 42px;
    color: #2c3e50;
    margin-bottom: 40px;
}

/* Cards container */
.cards-container {
    text-align: center;
    max-width: 1200px;
    margin: 0 auto;
}

/* Individual card */
.card {
    width: 300px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    margin: 10px;
    display: inline-block;
    vertical-align: top;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
}

/* Card image */
.card img {
    width: 100%;
    border-radius: 8px 8px 0 0;
    display: block;
}

/* Card content area */
.card-content {
    padding: 20px;
    text-align: left;
}

/* Card heading */
.card h2 {
    color: #2c3e50;
    margin-top: 0;
    margin-bottom: 10px;
    font-size: 24px;
}

/* Card paragraph */
.card p {
    line-height: 1.6;
    color: #666;
    margin-bottom: 20px;
    font-size: 14px;
}

/* Card link (button style) */
.card-link {
    display: inline-block;
    padding: 10px 20px;
    background-color: #3498db;
    color: white;
    text-decoration: none;
    border-radius: 4px;
    transition: background-color 0.3s ease;
}

.card-link:hover {
    background-color: #2980b9;
}
```

</details>
