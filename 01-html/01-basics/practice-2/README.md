# Practice 2: Personal Profile (Medium)

## Objective

Build a more comprehensive personal profile page that includes images, links, and various text formatting elements.

## Requirements

Create a file named `profile.html` that includes:

1. Proper HTML5 document structure
2. A page title: "Personal Profile - [Your Name]"
3. An `<h1>` heading with your name
4. A profile image (you can use a placeholder like `https://via.placeholder.com/200`)
   - Include an `alt` attribute describing the image
5. An "About Me" section with:
   - An `<h2>` heading
   - 2-3 paragraphs about yourself
   - Use `<strong>` to emphasize important words
   - Use `<em>` for any text you want italicized
6. A "Skills" section with:
   - An `<h2>` heading
   - An ordered list of at least 5 skills
7. A "Contact" section with:
   - An `<h2>` heading
   - Links to at least 2 social media profiles or websites
   - Each link should open in a new tab (use `target="_blank"`)
8. A horizontal rule (`<hr>`) to separate sections
9. A footer with the current year and copyright information

## Tips

- Use the `target="_blank"` attribute to make links open in new tabs
- The `<hr>` tag creates a horizontal line to separate content
- Use proper semantic structure with headings
- Test all your links to make sure they work

## Bonus Challenges

- Add a "Favorite Quote" section with a blockquote
- Include multiple images
- Add line breaks where appropriate using `<br>`

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
    <title>Personal Profile - Alex Johnson</title>
</head>
<body>
    <h1>Alex Johnson</h1>
    
    <img src="https://via.placeholder.com/200" alt="Profile picture of Alex Johnson">
    
    <hr>
    
    <h2>About Me</h2>
    <p>Hello! I'm <strong>Alex Johnson</strong>, a passionate web developer and lifelong learner. I love creating <em>beautiful and functional</em> websites that make a difference.</p>
    <p>When I'm not coding, you can find me exploring the outdoors, reading science fiction novels, or experimenting with new recipes in the kitchen. I believe that <strong>creativity and technology</strong> go hand in hand.</p>
    <p>I'm currently learning HTML, CSS, and JavaScript to build my web development skills and create amazing user experiences.</p>
    
    <hr>
    
    <h2>Skills</h2>
    <ol>
        <li>HTML5</li>
        <li>Problem Solving</li>
        <li>Creative Thinking</li>
        <li>Communication</li>
        <li>Time Management</li>
    </ol>
    
    <hr>
    
    <h2>Contact</h2>
    <p>Connect with me online:</p>
    <ul>
        <li><a href="https://github.com/alexjohnson" target="_blank">GitHub Profile</a></li>
        <li><a href="https://linkedin.com/in/alexjohnson" target="_blank">LinkedIn Profile</a></li>
        <li><a href="https://twitter.com/alexjohnson" target="_blank">Twitter</a></li>
    </ul>
    
    <hr>
    
    <p>&copy; 2024 Alex Johnson. All rights reserved.</p>
</body>
</html>
```

</details>
