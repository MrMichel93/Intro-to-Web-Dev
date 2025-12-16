# Practice 2: Registration Form (Medium)

## Objective

Build a user registration form that includes various input types, validation, and proper form structure. This exercise will help you work with different input types and attributes.

## Requirements

Create a file named `register.html` that includes:

1. Proper HTML5 document structure
2. A page title: "User Registration"
3. An `<h1>` heading: "Create Your Account"
4. A registration form with:
   - **Username** (text input, required, minlength 3, maxlength 20)
   - **Email** (email input, required)
   - **Password** (password input, required, minlength 8)
   - **Confirm Password** (password input, required)
   - **Date of Birth** (date input, required)
   - **Gender** (radio buttons: Male, Female, Other)
   - **Country** (dropdown with at least 5 countries)
   - **Terms and Conditions** (checkbox, required)
     - Include a label: "I agree to the terms and conditions"
   - **Newsletter** (checkbox, optional)
     - Include a label: "Subscribe to newsletter"
5. Two buttons:
   - Submit button: "Register"
   - Reset button: "Clear Form"
6. Use a `<fieldset>` with a `<legend>` for the gender section

## Tips

- Use the `required` attribute for mandatory fields
- Use `minlength` and `maxlength` for validation
- Group radio buttons with the same `name` attribute
- Use descriptive placeholder text
- The `<fieldset>` and `<legend>` tags help organize related inputs

## Bonus Challenges

- Add a phone number field with appropriate input type
- Add a bio/about section with a textarea
- Include a profile picture upload field
- Add pattern validation for the username (alphanumeric only)

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
    <title>User Registration</title>
</head>
<body>
    <h1>Create Your Account</h1>
    
    <form action="#" method="POST">
        <label for="username">Username:</label><br>
        <input type="text" id="username" name="username" 
               placeholder="Choose a username" 
               required minlength="3" maxlength="20"><br><br>
        
        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" 
               placeholder="your.email@example.com" required><br><br>
        
        <label for="password">Password:</label><br>
        <input type="password" id="password" name="password" 
               placeholder="At least 8 characters" 
               required minlength="8"><br><br>
        
        <label for="confirm-password">Confirm Password:</label><br>
        <input type="password" id="confirm-password" name="confirm-password" 
               placeholder="Re-enter your password" required><br><br>
        
        <label for="dob">Date of Birth:</label><br>
        <input type="date" id="dob" name="dob" required><br><br>
        
        <fieldset>
            <legend>Gender:</legend>
            <input type="radio" id="male" name="gender" value="male">
            <label for="male">Male</label><br>
            
            <input type="radio" id="female" name="gender" value="female">
            <label for="female">Female</label><br>
            
            <input type="radio" id="other" name="gender" value="other">
            <label for="other">Other</label>
        </fieldset><br>
        
        <label for="country">Country:</label><br>
        <select id="country" name="country" required>
            <option value="">Select your country</option>
            <option value="usa">United States</option>
            <option value="canada">Canada</option>
            <option value="uk">United Kingdom</option>
            <option value="australia">Australia</option>
            <option value="germany">Germany</option>
            <option value="other">Other</option>
        </select><br><br>
        
        <input type="checkbox" id="terms" name="terms" required>
        <label for="terms">I agree to the terms and conditions</label><br>
        
        <input type="checkbox" id="newsletter" name="newsletter">
        <label for="newsletter">Subscribe to newsletter</label><br><br>
        
        <button type="submit">Register</button>
        <button type="reset">Clear Form</button>
    </form>
</body>
</html>
```

</details>
