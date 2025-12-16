# Practice 1: Contact Form (Easy)

## Objective

Create a simple contact form that allows users to send a message. This will help you understand basic form structure and input fields.

## Requirements

Create a file named `contact.html` that includes:

1. Proper HTML5 document structure
2. A page title: "Contact Us"
3. An `<h1>` heading: "Contact Us"
4. A brief paragraph encouraging users to get in touch
5. A form with the following fields:
   - **Name** (text input, required)
   - **Email** (email input, required)
   - **Subject** (text input)
   - **Message** (textarea, required, at least 4 rows)
6. A submit button with the text "Send Message"
7. Proper labels for each input field
8. The form should have `action="#"` and `method="POST"`

## Tips

- Use `<label>` tags with matching `for` attributes
- Add the `required` attribute to mandatory fields
- Use the `placeholder` attribute to provide hints
- Set appropriate `rows` and `cols` for the textarea

## Example Output

```
Contact Us

We'd love to hear from you! Fill out the form below and we'll get back to you soon.

Name: [___________________]
Email: [___________________]
Subject: [___________________]
Message: [___________________]
         [___________________]
         [___________________]

[Send Message]
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
    <title>Contact Us</title>
</head>
<body>
    <h1>Contact Us</h1>
    
    <p>We'd love to hear from you! Fill out the form below and we'll get back to you as soon as possible.</p>
    
    <form action="#" method="POST">
        <label for="name">Name:</label><br>
        <input type="text" id="name" name="name" placeholder="Your full name" required><br><br>
        
        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" placeholder="your.email@example.com" required><br><br>
        
        <label for="subject">Subject:</label><br>
        <input type="text" id="subject" name="subject" placeholder="What is this about?"><br><br>
        
        <label for="message">Message:</label><br>
        <textarea id="message" name="message" rows="6" cols="50" placeholder="Your message here..." required></textarea><br><br>
        
        <button type="submit">Send Message</button>
    </form>
</body>
</html>
```

</details>
