# Practice 3: Responsive Website Layout (Hard)

## Objective

Create a complete responsive website layout combining Grid, Flexbox, and media queries.

## Requirements

Build a full page with:
1. Fixed/sticky header with logo and navigation
2. Hero section with centered content
3. Three-column feature section
4. Two-column content section (main + sidebar)
5. Footer with multiple columns
6. Fully responsive (mobile, tablet, desktop)

## Solution

<details>
<summary>Click to see solution</summary>

**website.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="header">
        <div class="container">
            <div class="logo">MyBrand</div>
            <nav>
                <a href="#home">Home</a>
                <a href="#features">Features</a>
                <a href="#about">About</a>
                <a href="#contact">Contact</a>
            </nav>
        </div>
    </header>
    
    <section class="hero">
        <div class="hero-content">
            <h1>Welcome to Our Website</h1>
            <p>Building amazing digital experiences</p>
            <button>Get Started</button>
        </div>
    </section>
    
    <section class="features">
        <div class="container">
            <h2>Our Features</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <h3>Fast</h3>
                    <p>Lightning fast performance</p>
                </div>
                <div class="feature-card">
                    <h3>Secure</h3>
                    <p>Top-notch security</p>
                </div>
                <div class="feature-card">
                    <h3>Reliable</h3>
                    <p>99.9% uptime guarantee</p>
                </div>
            </div>
        </div>
    </section>
    
    <section class="content-section">
        <div class="container">
            <div class="two-column">
                <main class="main-content">
                    <h2>Main Content</h2>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
                    <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
                </main>
                <aside class="sidebar">
                    <h3>Sidebar</h3>
                    <ul>
                        <li>Related Link 1</li>
                        <li>Related Link 2</li>
                        <li>Related Link 3</li>
                    </ul>
                </aside>
            </div>
        </div>
    </section>
    
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div>
                    <h4>Company</h4>
                    <ul>
                        <li><a href="#about">About</a></li>
                        <li><a href="#careers">Careers</a></li>
                    </ul>
                </div>
                <div>
                    <h4>Products</h4>
                    <ul>
                        <li><a href="#product1">Product 1</a></li>
                        <li><a href="#product2">Product 2</a></li>
                    </ul>
                </div>
                <div>
                    <h4>Contact</h4>
                    <p>Email: info@example.com</p>
                </div>
            </div>
            <p class="copyright">&copy; 2024 MyBrand</p>
        </div>
    </footer>
</body>
</html>
```

**styles.css:**
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Header */
.header {
    background-color: #2c3e50;
    color: white;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 20px;
}

.logo {
    font-size: 24px;
    font-weight: bold;
}

.header nav {
    display: flex;
    gap: 20px;
}

.header nav a {
    color: white;
    text-decoration: none;
}

.header nav a:hover {
    color: #3498db;
}

/* Hero */
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 100px 20px;
    text-align: center;
}

.hero-content h1 {
    font-size: 48px;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 20px;
    margin-bottom: 30px;
}

.hero-content button {
    background-color: white;
    color: #667eea;
    border: none;
    padding: 15px 30px;
    font-size: 16px;
    border-radius: 5px;
    cursor: pointer;
}

/* Features */
.features {
    padding: 60px 0;
}

.features h2 {
    text-align: center;
    margin-bottom: 40px;
    font-size: 36px;
}

.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
}

.feature-card {
    background-color: #f8f9fa;
    padding: 30px;
    border-radius: 8px;
    text-align: center;
}

.feature-card h3 {
    color: #2c3e50;
    margin-bottom: 10px;
}

/* Content Section */
.content-section {
    padding: 60px 0;
    background-color: #f8f9fa;
}

.two-column {
    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 40px;
}

.main-content h2 {
    margin-bottom: 20px;
}

.main-content p {
    margin-bottom: 15px;
}

.sidebar {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
}

.sidebar ul {
    list-style: none;
}

.sidebar li {
    padding: 8px 0;
    border-bottom: 1px solid #eee;
}

/* Footer */
.footer {
    background-color: #2c3e50;
    color: white;
    padding: 40px 0 20px;
}

.footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    margin-bottom: 30px;
}

.footer h4 {
    margin-bottom: 15px;
}

.footer ul {
    list-style: none;
}

.footer a {
    color: #bdc3c7;
    text-decoration: none;
}

.copyright {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid #34495e;
}

/* Responsive */
@media (max-width: 768px) {
    .header .container {
        flex-direction: column;
        gap: 15px;
    }
    
    .hero-content h1 {
        font-size: 32px;
    }
    
    .two-column {
        grid-template-columns: 1fr;
    }
}
```

</details>
