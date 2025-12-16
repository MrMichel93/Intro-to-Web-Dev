# Practice 3: Portfolio Website (Hard)

## Objective

Create a complete, professional portfolio website using comprehensive semantic HTML structure. This exercise combines all your HTML knowledge including semantic elements, forms, and proper organization.

## Requirements

Create a file named `portfolio.html` that includes:

1. Proper HTML5 document structure with appropriate meta tags
2. A page title: "[Your Name] - Portfolio"

3. **Header Section** (`<header>`)
   - Your name as `<h1>`
   - Professional tagline/subtitle
   - Navigation menu (`<nav>`) with smooth scroll links to: About, Skills, Projects, Contact

4. **Hero/Introduction Section** (`<section id="about">`)
   - A heading "About Me"
   - Profile image with semantic markup
   - 2-3 paragraphs introducing yourself
   - Your professional background and interests

5. **Skills Section** (`<section id="skills">`)
   - Heading "My Skills"
   - Multiple `<article>` elements for skill categories:
     - Frontend Development (list of skills)
     - Backend Development (list of skills)
     - Tools & Technologies (list of skills)
   - Use semantic lists for skill items

6. **Projects Section** (`<section id="projects">`)
   - Heading "My Projects"
   - At least 3 `<article>` elements, each representing a project:
     - Project name as `<h3>`
     - Project image with caption (`<figure>` and `<figcaption>`)
     - Project description (2 paragraphs)
     - Technologies used (list)
     - Links to live demo and source code
     - Date completed (`<time>`)

7. **Experience/Timeline Section** (optional but recommended)
   - Use `<section>` with articles for different experiences
   - Include dates with `<time>` elements

8. **Testimonials Section** (optional)
   - Use `<section>` with `<article>` or `<blockquote>` elements
   - Include author citations

9. **Contact Section** (`<section id="contact">`)
   - Heading "Get In Touch"
   - Contact information using `<address>`
   - A contact form with:
     - Name field
     - Email field
     - Subject field
     - Message textarea
     - Submit button
   - Social media links

10. **Footer** (`<footer>`)
    - Copyright notice with current year
    - Quick links navigation
    - Social media icons/links
    - "Back to top" link

## Tips

- Use `id` attributes on sections for navigation links
- Implement proper heading hierarchy (h1 -> h2 -> h3)
- Use `<figure>` and `<figcaption>` for all images with captions
- Include `<time>` elements with datetime attributes
- Use `<address>` for contact information
- Ensure all forms have proper labels and attributes
- Consider using `<details>` and `<summary>` for expandable content

## Bonus Challenges

- Add a resume download section with a link to a PDF
- Include a blog section with recent posts
- Add a statistics section (using `<dl>` for definition lists)
- Create an interactive timeline using semantic HTML
- Include a certificates/awards section
- Add a "Fun Facts" aside section
- Include meta tags for SEO and social media sharing

## Solution

Try to complete this on your own first! This is a comprehensive exercise.

<details>
<summary>Click to see solution</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Alex Johnson's professional web development portfolio">
    <meta name="author" content="Alex Johnson">
    <title>Alex Johnson - Portfolio</title>
</head>
<body>
    <header id="top">
        <h1>Alex Johnson</h1>
        <p><strong>Full-Stack Web Developer</strong></p>
        <nav>
            <a href="#about">About</a> | 
            <a href="#skills">Skills</a> | 
            <a href="#projects">Projects</a> | 
            <a href="#contact">Contact</a>
        </nav>
    </header>
    
    <main>
        <!-- About Section -->
        <section id="about">
            <h2>About Me</h2>
            <figure>
                <img src="https://via.placeholder.com/300" alt="Professional photo of Alex Johnson">
                <figcaption>Alex Johnson - Web Developer</figcaption>
            </figure>
            <p>Hello! I'm <strong>Alex Johnson</strong>, a passionate full-stack web developer with a love for creating beautiful, functional, and user-friendly websites. I specialize in HTML, CSS, and JavaScript, and I'm constantly learning new technologies to expand my skillset.</p>
            <p>With a background in computer science and several years of experience in web development, I've worked on projects ranging from small business websites to large-scale web applications. I believe in writing clean, maintainable code and creating experiences that users love.</p>
            <p>When I'm not coding, you can find me contributing to open-source projects, reading tech blogs, or exploring the great outdoors. I'm always excited to take on new challenges and collaborate with other developers.</p>
        </section>
        
        <!-- Skills Section -->
        <section id="skills">
            <h2>My Skills</h2>
            
            <article>
                <h3>Frontend Development</h3>
                <ul>
                    <li>HTML5 & Semantic Markup</li>
                    <li>CSS3 & Responsive Design</li>
                    <li>JavaScript (ES6+)</li>
                    <li>React & Vue.js</li>
                    <li>Accessibility (WCAG)</li>
                </ul>
            </article>
            
            <article>
                <h3>Backend Development</h3>
                <ul>
                    <li>Node.js & Express</li>
                    <li>Python & Django</li>
                    <li>RESTful API Design</li>
                    <li>Database Management (SQL & NoSQL)</li>
                    <li>Authentication & Security</li>
                </ul>
            </article>
            
            <article>
                <h3>Tools & Technologies</h3>
                <ul>
                    <li>Git & GitHub</li>
                    <li>VS Code</li>
                    <li>Webpack & Build Tools</li>
                    <li>Testing (Jest, Mocha)</li>
                    <li>Deployment (AWS, Heroku)</li>
                </ul>
            </article>
        </section>
        
        <!-- Projects Section -->
        <section id="projects">
            <h2>My Projects</h2>
            
            <article>
                <h3>E-Commerce Platform</h3>
                <figure>
                    <img src="https://via.placeholder.com/600x300" alt="Screenshot of e-commerce platform homepage">
                    <figcaption>Modern e-commerce platform with seamless checkout</figcaption>
                </figure>
                <p>A fully functional e-commerce platform built with modern web technologies. Features include user authentication, product catalog, shopping cart, and secure payment processing.</p>
                <p>This project challenged me to implement complex state management, optimize performance for large product catalogs, and ensure security throughout the checkout process.</p>
                <p><strong>Technologies:</strong></p>
                <ul>
                    <li>React</li>
                    <li>Node.js & Express</li>
                    <li>MongoDB</li>
                    <li>Stripe API</li>
                </ul>
                <p>
                    <time datetime="2023-12-01">Completed: December 2023</time>
                </p>
                <p>
                    <a href="https://example.com/demo" target="_blank">View Live Demo</a> | 
                    <a href="https://github.com/alexjohnson/ecommerce" target="_blank">View Source Code</a>
                </p>
            </article>
            
            <article>
                <h3>Task Management Application</h3>
                <figure>
                    <img src="https://via.placeholder.com/600x300" alt="Screenshot of task management dashboard">
                    <figcaption>Intuitive task management with drag-and-drop functionality</figcaption>
                </figure>
                <p>A productivity app that helps teams organize and track their work. Features real-time collaboration, drag-and-drop task organization, and customizable workflows.</p>
                <p>Built with a focus on user experience and performance, this application can handle thousands of tasks without slowing down. I implemented real-time updates using WebSockets for seamless team collaboration.</p>
                <p><strong>Technologies:</strong></p>
                <ul>
                    <li>Vue.js</li>
                    <li>Python & Django</li>
                    <li>PostgreSQL</li>
                    <li>WebSockets</li>
                </ul>
                <p>
                    <time datetime="2023-09-15">Completed: September 2023</time>
                </p>
                <p>
                    <a href="https://example.com/taskapp" target="_blank">View Live Demo</a> | 
                    <a href="https://github.com/alexjohnson/taskapp" target="_blank">View Source Code</a>
                </p>
            </article>
            
            <article>
                <h3>Weather Dashboard</h3>
                <figure>
                    <img src="https://via.placeholder.com/600x300" alt="Screenshot of weather dashboard interface">
                    <figcaption>Real-time weather data with beautiful visualizations</figcaption>
                </figure>
                <p>A responsive weather application that provides current conditions, forecasts, and historical weather data. Features interactive charts and maps for data visualization.</p>
                <p>This project taught me about working with external APIs, handling asynchronous data, and creating responsive data visualizations that work across all device sizes.</p>
                <p><strong>Technologies:</strong></p>
                <ul>
                    <li>JavaScript (Vanilla)</li>
                    <li>Chart.js</li>
                    <li>OpenWeather API</li>
                    <li>HTML5 & CSS3</li>
                </ul>
                <p>
                    <time datetime="2023-07-20">Completed: July 2023</time>
                </p>
                <p>
                    <a href="https://example.com/weather" target="_blank">View Live Demo</a> | 
                    <a href="https://github.com/alexjohnson/weather" target="_blank">View Source Code</a>
                </p>
            </article>
        </section>
        
        <!-- Contact Section -->
        <section id="contact">
            <h2>Get In Touch</h2>
            <p>I'm always interested in hearing about new projects and opportunities. Feel free to reach out!</p>
            
            <address>
                <p><strong>Email:</strong> <a href="mailto:alex@example.com">alex@example.com</a></p>
                <p><strong>Phone:</strong> <a href="tel:+1234567890">+1 (234) 567-890</a></p>
                <p><strong>Location:</strong> San Francisco, CA</p>
            </address>
            
            <h3>Send Me a Message</h3>
            <form action="#" method="POST">
                <label for="name">Name:</label><br>
                <input type="text" id="name" name="name" required><br><br>
                
                <label for="email">Email:</label><br>
                <input type="email" id="email" name="email" required><br><br>
                
                <label for="subject">Subject:</label><br>
                <input type="text" id="subject" name="subject" required><br><br>
                
                <label for="message">Message:</label><br>
                <textarea id="message" name="message" rows="6" cols="50" required></textarea><br><br>
                
                <button type="submit">Send Message</button>
            </form>
            
            <h3>Connect With Me</h3>
            <nav>
                <a href="https://github.com/alexjohnson" target="_blank">GitHub</a> | 
                <a href="https://linkedin.com/in/alexjohnson" target="_blank">LinkedIn</a> | 
                <a href="https://twitter.com/alexjohnson" target="_blank">Twitter</a> | 
                <a href="https://codepen.io/alexjohnson" target="_blank">CodePen</a>
            </nav>
        </section>
    </main>
    
    <footer>
        <p>&copy; <time datetime="2024">2024</time> Alex Johnson. All rights reserved.</p>
        <nav>
            <a href="#top">Back to Top</a> | 
            <a href="#about">About</a> | 
            <a href="#projects">Projects</a> | 
            <a href="#contact">Contact</a>
        </nav>
        <p>
            <a href="https://github.com/alexjohnson" target="_blank">GitHub</a> | 
            <a href="https://linkedin.com/in/alexjohnson" target="_blank">LinkedIn</a> | 
            <a href="https://twitter.com/alexjohnson" target="_blank">Twitter</a>
        </p>
    </footer>
</body>
</html>
```

</details>
