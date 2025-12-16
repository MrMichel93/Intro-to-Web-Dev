# Practice 3: Navigation Menu (Hard)

## Objective

Build a styled, interactive navigation menu with hover effects, demonstrating advanced use of CSS selectors, pseudo-classes, and styling techniques.

## Requirements

Create two files:

**navigation.html** - An HTML page with:
1. Proper HTML5 structure
2. A link to `styles.css`
3. A header containing:
   - A logo/site name
   - A navigation menu with at least 5 links
   - One link should have a "Home" class (active page)
   - One link should be a dropdown with sub-items
4. Main content area with a heading and paragraph
5. Use semantic HTML (`<header>`, `<nav>`, `<main>`)

**styles.css** - A stylesheet that creates:

1. **Header:**
   - Background color (dark)
   - Padding
   - Box shadow
   - Fixed or static positioning

2. **Logo/Site name:**
   - Float left or inline
   - White color
   - Larger font size
   - No underline

3. **Navigation menu:**
   - Float right or inline
   - Remove default list styling
   - Horizontal layout (inline or inline-block items)

4. **Navigation links:**
   - Display: inline-block or inline
   - Padding: 15px 20px
   - Color: white
   - No underline
   - Transition for smooth effects

5. **Link hover effect:**
   - Background color change
   - Color change (optional)
   - Smooth transition

6. **Active link (.active):**
   - Different background color
   - Border bottom or other indicator

7. **Dropdown menu:**
   - Position: relative for parent
   - Position: absolute for dropdown
   - Hidden by default
   - Show on hover
   - Background color
   - Box shadow

8. **Dropdown items:**
   - Display: block
   - Padding
   - Hover effect
   - Border between items (optional)

9. **Main content:**
   - Max width for readability
   - Padding
   - Margin

## Tips

- Use `display: inline-block;` for horizontal menu items
- Use pseudo-class `:hover` for interactive effects
- For dropdown: parent has `position: relative;`, dropdown has `position: absolute;`
- Hide dropdown with `display: none;`, show with `display: block;` on parent hover
- Use `transition` for smooth animations
- Clear floats if using float layout

## Bonus Challenges

- Make the navigation sticky (fixed position)
- Add a hamburger icon for mobile (just visually, no JavaScript)
- Add icons to menu items
- Create a mega menu with multiple columns
- Add smooth scroll behavior
- Implement a search bar in the navigation

## Solution

Try to complete this on your own first!

<details>
<summary>Click to see solution</summary>

**navigation.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">
                <a href="#home">MyWebsite</a>
            </div>
            <nav>
                <ul class="nav-menu">
                    <li><a href="#home" class="active">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li class="dropdown">
                        <a href="#services">Services</a>
                        <ul class="dropdown-menu">
                            <li><a href="#web-design">Web Design</a></li>
                            <li><a href="#development">Development</a></li>
                            <li><a href="#consulting">Consulting</a></li>
                        </ul>
                    </li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <main>
        <div class="container">
            <h1>Welcome to Our Website</h1>
            <p>This is a demonstration of a styled navigation menu with hover effects and a dropdown submenu. The navigation is clean, modern, and user-friendly.</p>
            <p>Try hovering over the menu items to see the interactive effects. The "Services" menu item has a dropdown that appears when you hover over it.</p>
        </div>
    </main>
</body>
</html>
```

**styles.css:**
```css
/* Reset and universal styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
}

/* Container for content */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Header styles */
header {
    background-color: #2c3e50;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 0;
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
}

/* Logo styles */
.logo a {
    color: white;
    font-size: 28px;
    font-weight: bold;
    text-decoration: none;
    padding: 20px 0;
    display: inline-block;
}

.logo a:hover {
    color: #3498db;
}

/* Navigation menu */
.nav-menu {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
}

.nav-menu > li {
    position: relative;
}

.nav-menu > li > a {
    display: block;
    color: white;
    text-decoration: none;
    padding: 20px 20px;
    transition: background-color 0.3s ease, color 0.3s ease;
}

.nav-menu > li > a:hover {
    background-color: #34495e;
    color: #3498db;
}

/* Active link */
.nav-menu > li > a.active {
    background-color: #3498db;
    color: white;
}

/* Dropdown menu */
.dropdown {
    position: relative;
}

.dropdown-menu {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    background-color: #34495e;
    min-width: 200px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    list-style: none;
    padding: 0;
    margin: 0;
    z-index: 1000;
}

.dropdown:hover .dropdown-menu {
    display: block;
}

.dropdown-menu li {
    border-bottom: 1px solid #2c3e50;
}

.dropdown-menu li:last-child {
    border-bottom: none;
}

.dropdown-menu li a {
    display: block;
    color: white;
    text-decoration: none;
    padding: 12px 20px;
    transition: background-color 0.3s ease, padding-left 0.3s ease;
}

.dropdown-menu li a:hover {
    background-color: #2c3e50;
    padding-left: 25px;
}

/* Main content */
main {
    margin-top: 40px;
    margin-bottom: 40px;
}

main .container {
    max-width: 800px;
}

main h1 {
    color: #2c3e50;
    margin-bottom: 20px;
    font-size: 36px;
}

main p {
    color: #555;
    margin-bottom: 15px;
    font-size: 16px;
    line-height: 1.8;
}

/* Responsive adjustments (bonus) */
@media (max-width: 768px) {
    header .container {
        flex-direction: column;
        align-items: flex-start;
    }
    
    .nav-menu {
        flex-direction: column;
        width: 100%;
    }
    
    .nav-menu > li {
        width: 100%;
    }
    
    .dropdown-menu {
        position: static;
        box-shadow: none;
        display: none;
    }
    
    .dropdown:hover .dropdown-menu {
        display: block;
    }
}
```

</details>
