# Practice 2: Loading Animations (Medium)

## Objective
Create creative loading spinners and progress indicators using CSS animations.

## Requirements
Create 4 different loading animations:
1. Spinning circle/donut loader
2. Bouncing dots
3. Progress bar with animation
4. Pulsing rings

Use `@keyframes` and animation properties.

## Solution
<details>
<summary>View Solution</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loading Animations</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="loader-container">
        <div class="spinner"></div>
        <p>Spinner</p>
    </div>
    
    <div class="loader-container">
        <div class="dots">
            <div class="dot"></div>
            <div class="dot"></div>
            <div class="dot"></div>
        </div>
        <p>Bouncing Dots</p>
    </div>
    
    <div class="loader-container">
        <div class="progress-bar">
            <div class="progress-fill"></div>
        </div>
        <p>Progress Bar</p>
    </div>
    
    <div class="loader-container">
        <div class="pulse-ring"></div>
        <p>Pulse Ring</p>
    </div>
</body>
</html>
```

```css
body {
    font-family: Arial, sans-serif;
    background: #f5f5f5;
    padding: 50px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 40px;
}

.loader-container {
    text-align: center;
}

.loader-container p {
    margin-top: 20px;
    color: #333;
}

/* Spinner */
.spinner {
    width: 50px;
    height: 50px;
    border: 5px solid #f3f3f3;
    border-top: 5px solid #3498db;
    border-radius: 50%;
    animation: spin 1s linear infinite;
    margin: 0 auto;
}

@keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}

/* Bouncing Dots */
.dots {
    display: flex;
    gap: 10px;
    justify-content: center;
}

.dot {
    width: 15px;
    height: 15px;
    background: #3498db;
    border-radius: 50%;
    animation: bounce 1.4s infinite ease-in-out both;
}

.dot:nth-child(1) {
    animation-delay: -0.32s;
}

.dot:nth-child(2) {
    animation-delay: -0.16s;
}

@keyframes bounce {
    0%, 80%, 100% {
        transform: scale(0);
    }
    40% {
        transform: scale(1);
    }
}

/* Progress Bar */
.progress-bar {
    width: 200px;
    height: 20px;
    background: #f3f3f3;
    border-radius: 10px;
    overflow: hidden;
    margin: 0 auto;
}

.progress-fill {
    height: 100%;
    background: linear-gradient(90deg, #667eea, #764ba2);
    animation: progress 2s ease-in-out infinite;
}

@keyframes progress {
    0% { width: 0%; }
    50% { width: 100%; }
    100% { width: 0%; }
}

/* Pulse Ring */
.pulse-ring {
    width: 50px;
    height: 50px;
    border: 5px solid #3498db;
    border-radius: 50%;
    margin: 0 auto;
    animation: pulse 2s ease-out infinite;
}

@keyframes pulse {
    0% {
        transform: scale(0.8);
        opacity: 1;
    }
    100% {
        transform: scale(2);
        opacity: 0;
    }
}
```

</details>
