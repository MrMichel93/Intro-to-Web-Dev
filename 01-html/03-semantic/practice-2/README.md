# Practice 2: News Website (Medium)

## Objective

Build a news website homepage with multiple articles organized in sections, demonstrating proper use of semantic HTML for a more complex page structure.

## Requirements

Create a file named `news.html` that includes:

1. Proper HTML5 document structure
2. A page title: "Daily News - Your Source for News"
3. A `<header>` containing:
   - Site logo/name as `<h1>`
   - A `<nav>` with categories: Home, World, Technology, Sports, Entertainment
4. A `<main>` section containing:
   - **Featured Section** (`<section>`)
     - An `<h2>` heading "Featured Story"
     - One featured `<article>` with:
       - Headline (`<h3>`)
       - Author and date
       - Image with caption (use `<figure>` and `<figcaption>`)
       - 2-3 paragraphs
   - **Latest News Section** (`<section>`)
     - An `<h2>` heading "Latest News"
     - Three news `<article>` elements, each with:
       - Headline (`<h3>`)
       - Publication time (`<time>`)
       - Short summary (1 paragraph)
       - "Read more" link
5. An `<aside>` with:
   - **Trending Topics** (`<h3>`)
   - An unordered list of 5 trending topics
   - **Newsletter Signup** (`<h3>`)
   - A brief form (email input and subscribe button)
6. A `<footer>` containing:
   - Copyright notice
   - A `<nav>` with footer links (Privacy, Terms, Contact, About)
   - Social media links

## Tips

- Use `<section>` to group related articles
- Each article should have a clear heading hierarchy
- Use `<figure>` and `<figcaption>` for images with captions
- Include semantic time elements with datetime attributes
- Organize the footer with multiple elements

## Bonus Challenges

- Add a "Breaking News" section at the top
- Include a weather widget in the aside
- Add author information using `<address>` tags
- Create a "Most Popular" section with an ordered list

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
    <title>Daily News - Your Source for News</title>
</head>
<body>
    <header>
        <h1>Daily News</h1>
        <p><em>Your trusted source for news</em></p>
        <nav>
            <a href="#home">Home</a> | 
            <a href="#world">World</a> | 
            <a href="#tech">Technology</a> | 
            <a href="#sports">Sports</a> | 
            <a href="#entertainment">Entertainment</a>
        </nav>
    </header>
    
    <main>
        <!-- Featured Section -->
        <section>
            <h2>Featured Story</h2>
            <article>
                <h3>Major Breakthrough in Renewable Energy Technology</h3>
                <p>By Sarah Johnson | <time datetime="2024-01-15T10:30:00">January 15, 2024 at 10:30 AM</time></p>
                
                <figure>
                    <img src="https://via.placeholder.com/800x400" alt="Solar panels on modern building">
                    <figcaption>New solar technology promises to revolutionize clean energy</figcaption>
                </figure>
                
                <p>Scientists have announced a groundbreaking development in solar panel technology that could increase efficiency by up to 40%. This advancement represents a major step forward in the global transition to renewable energy sources.</p>
                
                <p>The new technology, developed by researchers at the International Energy Institute, uses a novel material composition that allows solar cells to capture a broader spectrum of light. This breakthrough could significantly reduce the cost of solar energy and accelerate its adoption worldwide.</p>
                
                <p>Industry experts are calling this one of the most significant advancements in renewable energy in the past decade, with potential applications ranging from residential rooftops to large-scale solar farms.</p>
            </article>
        </section>
        
        <!-- Latest News Section -->
        <section>
            <h2>Latest News</h2>
            
            <article>
                <h3>Tech Giants Announce New AI Collaboration</h3>
                <p>Published: <time datetime="2024-01-15T09:15:00">January 15, 2024 at 9:15 AM</time></p>
                <p>Leading technology companies have formed a new alliance to develop ethical AI standards and share research findings. The collaboration aims to ensure responsible AI development across the industry.</p>
                <p><a href="#">Read more</a></p>
            </article>
            
            <article>
                <h3>Global Summit Addresses Climate Change Action</h3>
                <p>Published: <time datetime="2024-01-15T08:00:00">January 15, 2024 at 8:00 AM</time></p>
                <p>World leaders gathered today to discuss concrete steps for reducing carbon emissions. The summit has resulted in several new commitments from participating nations to accelerate their climate goals.</p>
                <p><a href="#">Read more</a></p>
            </article>
            
            <article>
                <h3>Championship Game Sets New Viewership Records</h3>
                <p>Published: <time datetime="2024-01-14T22:30:00">January 14, 2024 at 10:30 PM</time></p>
                <p>Last night's championship game became the most-watched sporting event of the year, with millions tuning in worldwide. The thrilling match went into overtime, keeping viewers on the edge of their seats.</p>
                <p><a href="#">Read more</a></p>
            </article>
        </section>
    </main>
    
    <aside>
        <section>
            <h3>Trending Topics</h3>
            <ul>
                <li>Renewable Energy</li>
                <li>Artificial Intelligence</li>
                <li>Climate Summit</li>
                <li>Championship Sports</li>
                <li>Space Exploration</li>
            </ul>
        </section>
        
        <section>
            <h3>Newsletter Signup</h3>
            <p>Get the latest news delivered to your inbox!</p>
            <form action="#" method="POST">
                <input type="email" placeholder="Enter your email" required>
                <button type="submit">Subscribe</button>
            </form>
        </section>
    </aside>
    
    <footer>
        <p>&copy; 2024 Daily News. All rights reserved.</p>
        <nav>
            <a href="#privacy">Privacy Policy</a> | 
            <a href="#terms">Terms of Service</a> | 
            <a href="#contact">Contact Us</a> | 
            <a href="#about">About</a>
        </nav>
        <p>
            Follow us: 
            <a href="#twitter">Twitter</a> | 
            <a href="#facebook">Facebook</a> | 
            <a href="#instagram">Instagram</a>
        </p>
    </footer>
</body>
</html>
```

</details>
