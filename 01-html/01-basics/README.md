# HTML Basics

## Lesson Overview

HTML (HyperText Markup Language) is the standard markup language for creating web pages. It consists of elements represented by tags that tell the browser how to display content.

## Key Concepts

### 1. HTML Document Structure

Every HTML document has a basic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <!-- Your content goes here -->
</body>
</html>
```

- `<!DOCTYPE html>` - Declares this is an HTML5 document
- `<html>` - Root element of the page
- `<head>` - Contains meta information about the document
- `<body>` - Contains the visible content

### 2. Common HTML Tags

#### Headings
```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Smaller Heading</h3>
<!-- h1 through h6 available -->
```

#### Paragraphs and Text
```html
<p>This is a paragraph.</p>
<strong>Bold text</strong>
<em>Italic text</em>
<br> <!-- Line break -->
```

#### Links
```html
<a href="https://example.com">Click here</a>
<a href="about.html">About Page</a>
```

#### Images
```html
<img src="image.jpg" alt="Description of image">
```

#### Lists
```html
<!-- Unordered List -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
</ul>

<!-- Ordered List -->
<ol>
    <li>First item</li>
    <li>Second item</li>
</ol>
```

#### Divs and Spans
```html
<div>A block-level container</div>
<span>An inline container</span>
```

### 3. HTML Attributes

Tags can have attributes that provide additional information:

```html
<a href="https://example.com" target="_blank">Opens in new tab</a>
<img src="photo.jpg" alt="Description" width="300">
<p class="highlight">Paragraph with a class</p>
<div id="header">Div with an ID</div>
```

## Practice Problems

Complete these three exercises to reinforce your learning:

1. **[Practice 1: My First Web Page](./practice-1/README.md)** (Easy)
   - Create a basic HTML page with headings, paragraphs, and a list

2. **[Practice 2: Personal Profile](./practice-2/README.md)** (Medium)
   - Build a personal profile page with images, links, and various text formatting

3. **[Practice 3: Recipe Page](./practice-3/README.md)** (Hard)
   - Create a complete recipe page with multiple sections and nested lists

## Next Steps

Once you've completed all practice problems, move on to [HTML Forms and Input](../02-forms/README.md)!
