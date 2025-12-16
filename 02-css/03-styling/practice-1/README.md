# Practice 1: Animated Buttons (Easy)

## Objective
Create a collection of button styles with hover effects, transitions, and animations.

## Requirements
Create 5 different button styles:
1. Slide background button
2. Scale/grow on hover button
3. 3D push button
4. Glow effect button
5. Ripple effect button (using ::before/::after)

Each should have smooth transitions and creative hover effects.

## Tips
- Use `transition` for smooth changes
- Use `transform` for movement and scale
- Use `box-shadow` for depth and glow
- Use pseudo-elements for extra effects

## Solution
<details>
<summary>View Solution</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated Buttons</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Animated Button Collection</h1>
    <div class="button-container">
        <button class="btn slide-btn">Slide Background</button>
        <button class="btn grow-btn">Grow</button>
        <button class="btn push-btn">3D Push</button>
        <button class="btn glow-btn">Glow Effect</button>
        <button class="btn ripple-btn">Ripple</button>
    </div>
</body>
</html>
```

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    padding: 50px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    min-height: 100vh;
}

h1 {
    color: white;
    text-align: center;
    margin-bottom: 50px;
}

.button-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.btn {
    padding: 15px 30px;
    font-size: 16px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    position: relative;
    overflow: hidden;
}

.slide-btn {
    background: white;
    color: #667eea;
    transition: color 0.3s;
}

.slide-btn::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: #667eea;
    transition: left 0.3s;
    z-index: -1;
}

.slide-btn:hover {
    color: white;
}

.slide-btn:hover::before {
    left: 0;
}

.grow-btn {
    background: #3498db;
    color: white;
    transition: transform 0.3s ease;
}

.grow-btn:hover {
    transform: scale(1.1);
}

.push-btn {
    background: #e74c3c;
    color: white;
    box-shadow: 0 6px #c0392b;
    transition: all 0.1s;
}

.push-btn:hover {
    box-shadow: 0 4px #c0392b;
    transform: translateY(2px);
}

.push-btn:active {
    box-shadow: 0 0 #c0392b;
    transform: translateY(6px);
}

.glow-btn {
    background: #2ecc71;
    color: white;
    transition: box-shadow 0.3s;
}

.glow-btn:hover {
    box-shadow: 0 0 20px #2ecc71;
}

.ripple-btn {
    background: #f39c12;
    color: white;
}

.ripple-btn::after {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.5);
    transform: translate(-50%, -50%);
    transition: width 0.6s, height 0.6s;
}

.ripple-btn:hover::after {
    width: 300px;
    height: 300px;
}
```

</details>
