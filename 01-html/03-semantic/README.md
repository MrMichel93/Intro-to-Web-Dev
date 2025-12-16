# HTML Semantic Elements

## Lesson Overview

Semantic HTML uses meaningful tags that describe the content they contain. These elements make your code more readable, improve accessibility for screen readers, and help search engines understand your page structure better.

## Key Concepts

### 1. Why Use Semantic HTML?

- **Accessibility**: Screen readers can better navigate your content
- **SEO**: Search engines understand your page structure
- **Maintainability**: Code is easier to read and understand
- **Consistency**: Standard structure across web pages

### 2. Page Structure Elements

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Semantic Page</title>
</head>
<body>
    <header>
        <!-- Site header with logo, navigation -->
        <nav>
            <!-- Navigation links -->
        </nav>
    </header>
    
    <main>
        <!-- Main content of the page -->
        <article>
            <!-- Self-contained content -->
        </article>
        
        <section>
            <!-- Thematic grouping of content -->
        </section>
    </main>
    
    <aside>
        <!-- Side content, related links -->
    </aside>
    
    <footer>
        <!-- Footer with copyright, links -->
    </footer>
</body>
</html>
```

### 3. Common Semantic Elements

#### Header (`<header>`)
Contains introductory content or navigation. Can be used for the page header or within articles/sections.

```html
<header>
    <h1>My Website</h1>
    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
    </nav>
</header>
```

#### Nav (`<nav>`)
Contains navigation links for the site.

```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

#### Main (`<main>`)
Contains the main content of the page. Should be unique per page and not nested in other semantic elements.

```html
<main>
    <h1>Welcome to My Blog</h1>
    <p>This is the main content area.</p>
</main>
```

#### Article (`<article>`)
Represents independent, self-contained content that could be distributed separately.

```html
<article>
    <h2>Blog Post Title</h2>
    <p>Posted on <time datetime="2024-01-15">January 15, 2024</time></p>
    <p>Article content goes here...</p>
</article>
```

#### Section (`<section>`)
Represents a thematic grouping of content, typically with a heading.

```html
<section>
    <h2>About Us</h2>
    <p>Information about the company...</p>
</section>
```

#### Aside (`<aside>`)
Contains content tangentially related to the main content (sidebars, pull quotes, ads).

```html
<aside>
    <h3>Related Articles</h3>
    <ul>
        <li><a href="#">Article 1</a></li>
        <li><a href="#">Article 2</a></li>
    </ul>
</aside>
```

#### Footer (`<footer>`)
Contains footer information for its nearest ancestor or the page.

```html
<footer>
    <p>&copy; 2024 My Website. All rights reserved.</p>
    <nav>
        <a href="privacy.html">Privacy Policy</a>
        <a href="terms.html">Terms of Service</a>
    </nav>
</footer>
```

### 4. Content Semantic Elements

```html
<!-- Figure with caption -->
<figure>
    <img src="image.jpg" alt="Description">
    <figcaption>Image caption text</figcaption>
</figure>

<!-- Time/date -->
<p>Published on <time datetime="2024-01-15">January 15, 2024</time></p>

<!-- Mark (highlighted text) -->
<p>This is <mark>highlighted text</mark></p>

<!-- Address -->
<address>
    Written by <a href="mailto:john@example.com">John Doe</a><br>
    123 Main St, City, Country
</address>

<!-- Details/Summary (collapsible) -->
<details>
    <summary>Click to expand</summary>
    <p>Hidden content that can be toggled</p>
</details>
```

### 5. Semantic vs Non-Semantic

**Non-Semantic (avoid when semantic alternative exists):**
```html
<div id="header">
    <div id="nav">...</div>
</div>
<div id="content">...</div>
<div id="sidebar">...</div>
<div id="footer">...</div>
```

**Semantic (preferred):**
```html
<header>
    <nav>...</nav>
</header>
<main>...</main>
<aside>...</aside>
<footer>...</footer>
```

## Best Practices

1. Use semantic elements instead of generic `<div>` when appropriate
2. Each page should have one `<main>` element
3. Use `<article>` for content that makes sense on its own
4. Use `<section>` to group related content with a theme
5. Always include appropriate headings within semantic sections
6. Combine semantic elements (e.g., `<article>` can contain `<header>` and `<footer>`)

## Practice Problems

Complete these three exercises to master semantic HTML:

1. **[Practice 1: Blog Layout](./practice-1/README.md)** (Easy)
   - Create a simple blog page using semantic elements

2. **[Practice 2: News Website](./practice-2/README.md)** (Medium)
   - Build a news website homepage with multiple articles and sections

3. **[Practice 3: Portfolio Website](./practice-3/README.md)** (Hard)
   - Create a complete portfolio website with proper semantic structure

## Next Steps

Congratulations on completing the HTML section! Next, move on to [Part 2: CSS](../../02-css/README.md) to learn how to style your HTML!
