# Practice 1: Blog Layout (Easy)

## Objective

Create a simple blog page using semantic HTML elements to structure the content properly. This exercise will help you understand how to use `<header>`, `<main>`, `<article>`, `<aside>`, and `<footer>`.

## Requirements

Create a file named `blog.html` that includes:

1. Proper HTML5 document structure
2. A page title: "My Blog"
3. A `<header>` containing:
   - An `<h1>` with your blog name
   - A `<nav>` with at least 3 navigation links (Home, About, Contact)
4. A `<main>` section containing:
   - Two `<article>` elements, each with:
     - An `<h2>` for the post title
     - A `<time>` element showing the publish date
     - At least 2 paragraphs of content
5. An `<aside>` section with:
   - An `<h3>` heading "About the Author"
   - A paragraph about yourself
6. A `<footer>` with:
   - Copyright text
   - Your name

## Tips

- Use semantic elements instead of `<div>` tags
- Each article should be self-contained content
- The aside content is related but separate from the main content
- Include the `datetime` attribute in `<time>` elements

## Example Structure

```
===== HEADER =====
My Awesome Blog
[Home] [About] [Contact]

===== MAIN =====
Article 1: My First Post
Posted on January 15, 2024
[Content paragraphs...]

Article 2: Another Great Post
Posted on January 10, 2024
[Content paragraphs...]

===== ASIDE =====
About the Author
[Author bio...]

===== FOOTER =====
© 2024 Your Name
```

## Solution

Try to complete this on your own first!

<details>
<summary>Click to see solution</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Blog</title>
</head>
<body>
    <header>
        <h1>My Awesome Blog</h1>
        <nav>
            <a href="#home">Home</a> | 
            <a href="#about">About</a> | 
            <a href="#contact">Contact</a>
        </nav>
    </header>
    
    <main>
        <article>
            <h2>My First Blog Post</h2>
            <p>Posted on <time datetime="2024-01-15">January 15, 2024</time></p>
            <p>Welcome to my blog! I'm excited to share my thoughts and experiences with you. This is the beginning of an amazing journey into web development.</p>
            <p>In this blog, I'll be documenting my learning process, sharing tips and tricks, and discussing interesting topics in technology and programming.</p>
        </article>
        
        <article>
            <h2>Learning HTML - The Foundation of the Web</h2>
            <p>Posted on <time datetime="2024-01-10">January 10, 2024</time></p>
            <p>HTML is the backbone of every website. Understanding its structure and semantic elements is crucial for building accessible and well-organized web pages.</p>
            <p>Today I learned about semantic HTML elements like header, nav, main, article, aside, and footer. These elements not only make the code more readable but also improve SEO and accessibility.</p>
        </article>
    </main>
    
    <aside>
        <h3>About the Author</h3>
        <p>Hi! I'm a passionate web developer learning HTML, CSS, and JavaScript. I love creating beautiful and functional websites. When I'm not coding, you can find me reading tech blogs or exploring new frameworks.</p>
    </aside>
    
    <footer>
        <p>&copy; 2024 Alex Johnson. All rights reserved.</p>
    </footer>
</body>
</html>
```

</details>
