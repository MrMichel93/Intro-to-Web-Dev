# Practice 2: Grid Dashboard (Medium)

## Objective

Build a dashboard layout using CSS Grid with multiple content areas.

## Requirements

Create a dashboard with:
1. Header spanning full width
2. Sidebar for navigation
3. Main content area with stat cards
4. Stat cards in a responsive grid (2x2 or 3x3)
5. Footer spanning full width

Use CSS Grid for overall layout and nested grid for stat cards.

## Solution

<details>
<summary>Click to see solution</summary>

**dashboard.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="dashboard">
        <header class="header">
            <h1>Dashboard</h1>
        </header>
        
        <nav class="sidebar">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#analytics">Analytics</a></li>
                <li><a href="#reports">Reports</a></li>
                <li><a href="#settings">Settings</a></li>
            </ul>
        </nav>
        
        <main class="main-content">
            <h2>Statistics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <h3>Total Users</h3>
                    <p class="stat-number">1,234</p>
                </div>
                <div class="stat-card">
                    <h3>Revenue</h3>
                    <p class="stat-number">$45,678</p>
                </div>
                <div class="stat-card">
                    <h3>Orders</h3>
                    <p class="stat-number">567</p>
                </div>
                <div class="stat-card">
                    <h3>Growth</h3>
                    <p class="stat-number">+23%</p>
                </div>
            </div>
        </main>
        
        <footer class="footer">
            <p>&copy; 2024 Dashboard App</p>
        </footer>
    </div>
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
}

.dashboard {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
    grid-template-columns: 200px 1fr;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
}

.header {
    grid-area: header;
    background-color: #2c3e50;
    color: white;
    padding: 20px;
}

.sidebar {
    grid-area: sidebar;
    background-color: #34495e;
    padding: 20px;
}

.sidebar ul {
    list-style: none;
}

.sidebar a {
    display: block;
    color: white;
    text-decoration: none;
    padding: 10px;
    margin-bottom: 5px;
    border-radius: 4px;
}

.sidebar a:hover {
    background-color: #2c3e50;
}

.main-content {
    grid-area: main;
    padding: 30px;
    background-color: #ecf0f1;
}

.main-content h2 {
    margin-bottom: 20px;
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
}

.stat-card {
    background-color: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    text-align: center;
}

.stat-card h3 {
    color: #7f8c8d;
    font-size: 14px;
    margin-bottom: 10px;
}

.stat-number {
    font-size: 32px;
    font-weight: bold;
    color: #2c3e50;
}

.footer {
    grid-area: footer;
    background-color: #2c3e50;
    color: white;
    text-align: center;
    padding: 15px;
}

@media (max-width: 768px) {
    .dashboard {
        grid-template-areas:
            "header"
            "main"
            "sidebar"
            "footer";
        grid-template-columns: 1fr;
    }
}
```

</details>
