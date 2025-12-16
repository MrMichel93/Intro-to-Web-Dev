# Practice 3: Modern Landing Page (Hard)

## Objective
Create a stunning landing page combining all advanced CSS techniques: gradients, animations, glassmorphism, and more.

## Requirements

Build a complete landing page with:

1. **Hero Section:**
   - Full viewport height
   - Gradient background (animated)
   - Centered content with animated text
   - Call-to-action button with effects
   - Floating animation on an icon/image

2. **Features Section:**
   - 3 feature cards in a grid
   - Glassmorphism effect on cards
   - Hover effects (lift, glow, or scale)
   - Icons or images
   - Smooth transitions

3. **Statistics Section:**
   - 4 stat counters
   - Animated appearance (fade in from bottom)
   - Background with overlay

4. **CSS Techniques to Include:**
   - CSS custom properties (variables)
   - Linear/radial gradients
   - Backdrop-filter for glassmorphism
   - Keyframe animations
   - Transform and transitions
   - Box shadows
   - Smooth scroll behavior
   - Responsive design

## Solution

<details>
<summary>Click to see solution</summary>

**landing.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Landing Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <section class="hero">
        <div class="hero-content">
            <div class="floating-icon">✨</div>
            <h1 class="animated-title">Welcome to the Future</h1>
            <p class="subtitle">Discover amazing possibilities</p>
            <button class="cta-button">Get Started</button>
        </div>
    </section>
    
    <section class="features">
        <h2>Our Features</h2>
        <div class="features-grid">
            <div class="feature-card glass">
                <div class="icon">🚀</div>
                <h3>Fast Performance</h3>
                <p>Lightning-fast load times and smooth interactions</p>
            </div>
            <div class="feature-card glass">
                <div class="icon">🔒</div>
                <h3>Secure</h3>
                <p>Enterprise-grade security for your peace of mind</p>
            </div>
            <div class="feature-card glass">
                <div class="icon">💎</div>
                <h3>Premium Quality</h3>
                <p>Crafted with attention to every detail</p>
            </div>
        </div>
    </section>
    
    <section class="stats">
        <div class="stats-grid">
            <div class="stat fade-in">
                <h3>10K+</h3>
                <p>Happy Users</p>
            </div>
            <div class="stat fade-in">
                <h3>50+</h3>
                <p>Countries</p>
            </div>
            <div class="stat fade-in">
                <h3>99.9%</h3>
                <p>Uptime</p>
            </div>
            <div class="stat fade-in">
                <h3>24/7</h3>
                <p>Support</p>
            </div>
        </div>
    </section>
</body>
</html>
```

**styles.css:**
```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
    --text-light: #ffffff;
    --text-dark: #2d3748;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
}

/* Hero Section */
.hero {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    background-size: 200% 200%;
    animation: gradientShift 10s ease infinite;
    position: relative;
    overflow: hidden;
}

@keyframes gradientShift {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.hero-content {
    text-align: center;
    color: var(--text-light);
    z-index: 2;
}

.floating-icon {
    font-size: 80px;
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
}

.animated-title {
    font-size: 4rem;
    margin: 20px 0;
    animation: fadeInUp 1s ease;
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.subtitle {
    font-size: 1.5rem;
    margin-bottom: 30px;
    animation: fadeInUp 1s ease 0.3s both;
}

.cta-button {
    padding: 15px 40px;
    font-size: 1.1rem;
    background: white;
    color: var(--primary-color);
    border: none;
    border-radius: 50px;
    cursor: pointer;
    font-weight: bold;
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
    transition: all 0.3s ease;
    animation: fadeInUp 1s ease 0.6s both;
}

.cta-button:hover {
    transform: translateY(-3px) scale(1.05);
    box-shadow: 0 15px 40px rgba(0,0,0,0.4);
}

/* Features Section */
.features {
    padding: 100px 20px;
    background: linear-gradient(180deg, #f7fafc 0%, #edf2f7 100%);
}

.features h2 {
    text-align: center;
    font-size: 3rem;
    color: var(--text-dark);
    margin-bottom: 60px;
}

.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 40px;
    max-width: 1200px;
    margin: 0 auto;
}

.feature-card {
    padding: 40px;
    text-align: center;
    border-radius: 20px;
    transition: all 0.3s ease;
}

.glass {
    background: rgba(255, 255, 255, 0.25);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.3);
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
}

.feature-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
}

.icon {
    font-size: 4rem;
    margin-bottom: 20px;
}

.feature-card h3 {
    font-size: 1.5rem;
    color: var(--text-dark);
    margin-bottom: 15px;
}

.feature-card p {
    color: #4a5568;
}

/* Stats Section */
.stats {
    padding: 100px 20px;
    background: linear-gradient(135deg, var(--primary-color), var(--accent-color));
    color: white;
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 40px;
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;
}

.stat {
    opacity: 0;
    animation: fadeIn 1s ease forwards;
}

.stat:nth-child(1) { animation-delay: 0.2s; }
.stat:nth-child(2) { animation-delay: 0.4s; }
.stat:nth-child(3) { animation-delay: 0.6s; }
.stat:nth-child(4) { animation-delay: 0.8s; }

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.stat h3 {
    font-size: 3rem;
    margin-bottom: 10px;
}

/* Responsive */
@media (max-width: 768px) {
    .animated-title {
        font-size: 2.5rem;
    }
    
    .subtitle {
        font-size: 1.2rem;
    }
    
    .features h2 {
        font-size: 2rem;
    }
}
```

</details>
