# Practice 1: Flexbox Photo Gallery (Easy)

## Objective

Create a responsive photo gallery using Flexbox that adapts to different screen sizes.

## Requirements

Create `gallery.html` and `styles.css`:

1. HTML with 9-12 images (use placeholders)
2. Images in a container with class `gallery`
3. Use Flexbox to create a responsive grid
4. Images should wrap to new lines
5. Equal spacing between images
6. Images scale proportionally

## Flexbox Properties to Use

- `display: flex`
- `flex-wrap: wrap`
- `justify-content: space-around` or `space-between`
- `gap` for spacing
- Flex items should have consistent sizing

## Solution

<details>
<summary>Click to see solution</summary>

**gallery.html:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Photo Gallery</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>My Photo Gallery</h1>
    <div class="gallery">
        <img src="https://via.placeholder.com/300" alt="Photo 1">
        <img src="https://via.placeholder.com/300" alt="Photo 2">
        <img src="https://via.placeholder.com/300" alt="Photo 3">
        <img src="https://via.placeholder.com/300" alt="Photo 4">
        <img src="https://via.placeholder.com/300" alt="Photo 5">
        <img src="https://via.placeholder.com/300" alt="Photo 6">
        <img src="https://via.placeholder.com/300" alt="Photo 7">
        <img src="https://via.placeholder.com/300" alt="Photo 8">
        <img src="https://via.placeholder.com/300" alt="Photo 9">
    </div>
</body>
</html>
```

**styles.css:**
```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    padding: 20px;
    background-color: #f5f5f5;
}

h1 {
    text-align: center;
    margin-bottom: 30px;
    color: #333;
}

.gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    justify-content: center;
}

.gallery img {
    width: 300px;
    height: 300px;
    object-fit: cover;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
}

.gallery img:hover {
    transform: scale(1.05);
}

@media (max-width: 768px) {
    .gallery img {
        width: calc(50% - 10px);
    }
}

@media (max-width: 480px) {
    .gallery img {
        width: 100%;
    }
}
```

</details>
